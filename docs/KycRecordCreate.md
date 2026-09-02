# SimplebillyApi::KycRecordCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | Referenz auf den Kunden/Kontakt. | [optional] |
| **customer_name** | **String** | Name des Kunden (für die Suche). | [optional] |
| **kyc_date** | **Date** | Datum der KYC-Prüfung (GwG § 8). | [optional] |
| **notes** | **String** | Freitext-Notizen. | [optional] |
| **retention_until** | **Date** | Aufbewahrungsfrist (GwG § 8 Abs. 4: 5 Jahre). | [optional] |
| **risk_assessment** | **String** | Risikoeinschätzung (z. B. Risikoklasse). | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::KycRecordCreate.new(
  customer_id: null,
  customer_name: null,
  kyc_date: null,
  notes: null,
  retention_until: null,
  risk_assessment: null
)
```

