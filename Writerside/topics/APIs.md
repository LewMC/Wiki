# APIs

## Version API
Get information about the latest version of a resource.

https://service.lewmc.net/latest-version?resource=[RESOURCE]

You can also get a simple format by adding &format=simpleversion to the end.

Example (Full): https://service.lewmc.net/download-counter?resource=essence

Example (Simple): https://service.lewmc.net/download-counter?resource=essence&format=simpleversion

## Download Counter API

Get the number of downloads for a resource.

https://service.lewmc.net/download-counter?resource=[RESOURCE]

Adding &format=true to the URL formats the number counts as strings with commas for values over 1,000.

Resources: 'galactica', 'lews-jurassic-pack', 'lews-client-pack', 'simplyaesthetic', 'essence', 'kryptonite', 'all'

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

## Privacy

The API does not collect any information about you, our hosting provider may collect some data for security purposes, we do not have access to this. We can see how many people have used an endpoint via our hosting provider's dashboard, but we can not see who accessed it.

There are no rate limits, please be respectful and use the API appropriately so we do not have to implement this.

For terms and legal stuff visit [service.lewmc.net](https://service.lewmc.net).