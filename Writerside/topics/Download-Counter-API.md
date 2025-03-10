# Download Counter API

<warning>
If you're having issues with our APIs, try adding a "/" before the "?"
</warning>

> Base URL: https://service.lewmc.net

Get the number of downloads for a resource.

https://service.lewmc.net/download-counter?resource=[RESOURCE]

Adding &format=true to the URL formats the number counts as strings with commas for values over 1,000.

Results from this API are cached for 24 hours.

<api-doc openapi-path="../openapi/download-counter.yml"></api-doc>

## Resources
| Resource            | Description                                 | Version API | Download Counter API |
|---------------------|---------------------------------------------|-------------|----------------------|
| galactica           | The Galactica Modpack                       | ✅           | ✅                    |
| lewsjurassicpack    | The Lew's Jurassic Pack Modpack             | ✅           | ✅                    |
| lewsclientpack      | The Lew's Client Pack Modpack               | ✅           | ✅                    |
| simplyaesthetic     | The SimplyAesthetic Modpack                 | ✅           | ✅                    |
| essence             | The Essence Plugin                          | ✅           | ✅                    |
| essence-snapshot    | The Essence Plugin's snapshot/git branch    | ✅           | ❌                    |
| kryptonite          | The Kryptonite Plugin                       | ✅           | ✅                    |
| kryptonite-snapshot | The Kryptonite Plugin's snapshot/git branch | ✅           | ❌                    |
The essence-snapshot and kryptonite-snapshot download counts are bundled with release variants in essence and kryptonite resources.

Downloads from LewMC's legacy download system are not supported.