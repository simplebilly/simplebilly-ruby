# SimplebillyApi::DeclarationCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **declaration_type** | [**DeclarationType**](DeclarationType.md) | Art der Erklärung: \&quot;dcgk\&quot; (Entsprechenserklärung § 161 AktG) oder \&quot;unternehmensfuehrung\&quot; (Erklärung zur Unternehmensführung § 289f HGB). | [optional] |
| **is_current** | **Boolean** | Kennzeichnet die aktuell gültige Fassung (max. eine je Mandant). | [optional] |
| **text** | **String** | Inhalt der Erklärung als Markdown. | [optional] |
| **valid_from** | **Date** | Datum, ab dem die Erklärung gilt. | [optional] |
| **version** | **String** | Versionsbezeichnung der Erklärung (z.B. \&quot;2025-01\&quot;). | [optional] |

## Example

```ruby
require 'simplebilly_api'

instance = SimplebillyApi::DeclarationCreate.new(
  declaration_type: null,
  is_current: null,
  text: null,
  valid_from: null,
  version: null
)
```

