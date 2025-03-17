# Bravoure Workflow Templates

Deze directory bevat workflow templates die kunnen worden gebruikt in alle Bravoure repositories.

## Beschikbare Templates

### ClickUp PR Review Integration

Deze workflow voegt automatisch tags toe aan ClickUp taken en plaatst opmerkingen met review-informatie wanneer een gerelateerde Pull Request wordt goedgekeurd of wanneer er wijzigingen worden gevraagd op GitHub.

#### Vereisten

1. **ClickUp API Key**: Je moet je ClickUp API key toevoegen als een GitHub repository secret met de naam `CLICKUP_API_KEY`.

   Om deze secret aan te maken:
   - Ga naar je GitHub repository
   - Navigeer naar Settings > Secrets and variables > Actions
   - Klik op "New repository secret"
   - Naam: `CLICKUP_API_KEY`
   - Waarde: Je ClickUp API key

2. **ClickUp Tags**: Zorg ervoor dat de volgende tags bestaan in je ClickUp workspace:
   - `Pull request approved` - Voor goedgekeurde PR's
   - `Changes requested on pull request` - Voor PR's waar wijzigingen zijn gevraagd

#### Taak-ID formaat

De workflow zoekt naar ClickUp taak-ID's in de volgende formaten:
- `CU-abc123` of `cu-abc123` (hoofdletterongevoelig)
- `CU_abc123` of `cu_abc123` (hoofdletterongevoelig)
- `#abc123`

Zorg ervoor dat je branch namen, PR titels of commit berichten het taak-ID in een van deze formaten bevatten. 