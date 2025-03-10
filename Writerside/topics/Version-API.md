# Version API

<warning>
If you're having issues with our APIs, try adding a "/" before the "?"
</warning>

> Base URL: https://service.lewmc.net

Get information about the latest version of a resource.

https://service.lewmc.net/latest-version?resource=[RESOURCE]

You can also get a simple format by adding &format=simpleversion to the end.

Example (Full): https://service.lewmc.net/download-counter?resource=essence

Example (Simple): https://service.lewmc.net/download-counter?resource=essence&format=simpleversion

<api-doc openapi-path="../openapi/service-version.yml"></api-doc> 

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
