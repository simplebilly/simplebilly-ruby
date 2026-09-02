# SimplebillyApi::Participation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **acquired_at** | **Date** | Datum des Erwerbs der Beteiligung. | [optional] |
| **board_appointment** | **Boolean** | Bestellungsrecht für Geschäftsführung/Aufsichtsrat (§ 290 Abs. 2 Nr. 2 HGB). | [optional] |
| **company_name** | **String** | Name des Beteiligungsunternehmens (§ 271 HGB). | [optional] |
| **control_agreement** | **Boolean** | Beherrschungsvertrag (§ 290 Abs. 2 Nr. 3 HGB). | [optional] |
| **legal_form** | **String** | Rechtsform, z. B. \&quot;GmbH\&quot;. | [optional] |
| **ownership_pct** | **String** | Anteilsquote in Prozent (§ 271 HGB; &gt; 20 % widerlegbare Vermutung). | [optional] |
| **purpose_vehicle** | **Boolean** | Zweckgesellschaft (§ 290 Abs. 2 Nr. 4 HGB). | [optional] |
| **voting_majority** | **Boolean** | Stimmrechtsmehrheit (§ 290 Abs. 2 Nr. 1 HGB). | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::Participation.new(
  acquired_at: null,
  board_appointment: null,
  company_name: null,
  control_agreement: null,
  legal_form: null,
  ownership_pct: null,
  purpose_vehicle: null,
  voting_majority: null
)
```

