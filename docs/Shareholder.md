# SimplebillyApi::Shareholder

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address** | **String** | Anschrift des Aktionärs (§ 67 Abs. 1 AktG). | [optional] |
| **birth_date** | **Date** | Geburtsdatum des Aktionärs (§ 67 Abs. 1 AktG). | [optional] |
| **email** | **String** | Elektronische Adresse (E-Mail) für die Kommunikation der Gesellschaft. | [optional] |
| **first_name** | **String** | Vorname des Aktionärs (§ 67 Abs. 1 AktG). | [optional] |
| **last_name** | **String** | Nachname des Aktionärs (§ 67 Abs. 1 AktG). | [optional] |
| **share_number** | **String** | Aktiennummer bzw. Sammelurkunde (bei Nennbetragsaktien). | [optional] |
| **shares** | **String** | Stückzahl der gehaltenen Stückaktien (§ 67 Abs. 1 AktG). | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Shareholder.new(
  address: null,
  birth_date: null,
  email: null,
  first_name: null,
  last_name: null,
  share_number: null,
  shares: null
)
```

