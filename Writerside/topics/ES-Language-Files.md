# Supported Languages

| Language             | Code  | Supported                                        | Since |
|----------------------|-------|--------------------------------------------------|-------|
| Bengali              | bn-BD | ❌ File exists but is not enabled, not translated | 1.6.0 |
| British English      | en-GB | ✅ Fully                                          | 1.0.0 |
| Chinese (Simplified) | zn-CN | ✅ Fully                                          | 1.6.0 |
| French               | fr-FR | ❌ File exists but is not enabled, not translated | 1.6.0 |
| German               | de-DE | ❌ File exists but is not enabled, not translated | 1.6.0 |
| Hindi                | hi-IN | ❌ File exists but is not enabled, not translated | 1.6.0 |
| Japanese             | ja-JP | ❌ File exists but is not enabled, not translated | 1.6.0 |
| Korean               | ko-KR | ❌ File exists but is not enabled, not translated | 1.6.0 |
| Portuguese           | pt-PT | ❌ File exists but is not enabled, not translated | 1.6.0 |
| Spanish              | es-ES | ❌ File exists but is not enabled, not translated | 1.6.0 |
| Turkish              | tr-TR | ❌ File exists but is not enabled, not translated | 1.6.0 |
| Vietnamese           | vi-VN | ❌ File exists but is not enabled, not translated | 1.6.0 |

## Translate Essence
We use Crowdin to provide translations for Essence, it automatically synchronises to our GitHub repository so any changes are automatically pushed with the next Essence update.

Translate to Crowdin: [https://crowdin.com/project/lewmc-essence](https://crowdin.com/project/lewmc-essence)

## Language Files

Language files are used in Essence to serve messages to players

These are automatically updated whenever you update your plugin.

### Creating a new Language File
> Please consider translating essence to [Crowdin](https://crowdin.com/project/lewmc-essence) so that others can use the language too!
1. Create a new .yml file in the /plugins/essence/languages folder. You should give it a unique name such as custom.yml
2. Copy the contents of en-gb.yml to this file.
3. Customise any messages you wish to.
4. Change the language option in config.yml to the name of your file without the yml ending (e.g. "custom").