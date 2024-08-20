```mermaid
   sequenceDiagram
autoNumber
ML Connector ->> CC: POST /quote-requests /{}
CC->> CC:Validation Check, Quote Validation, Expiration Check
Alt if not Successful
CC-->>ML Connector: Response 500
End
CC->>CC:Calculate Charge
CC-->>ML Connector: Repsonse 200
```
