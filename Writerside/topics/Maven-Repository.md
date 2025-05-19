# Maven Repository

[Access the Repository](https://repo.lewmc.net)

Our Maven Repository is an automatic builder of our Java code.
It's used to provide access to our latest software.

We have two repositories available: `releases` and `snapshots`.

- `releases` contains stable, released software. These are the same jarfiles that we post on the various plugin marketplaces.
- `snapshots` contains in development, unreleased software. These jarfiles are updated with every push to GitHub and may be unstable and buggy. Use at your own risk.

## Using the LewMC Repository

### For downloading plugins
You can [access the repository](https://repo.lewmc.net) in your web browser, and use the buttons on screen to navigate to the plugin you'd like to download.

For stable plugins use the `releases` branch, if you'd like pre-release software use `snapshots`.

All of our plugins are under `net.lewmc` within the branch.

### For development
In Maven, you can add the repository as shown below, replacing `{repository}` with the name of the repo branch.
```xml
<repository>
  <id>lewmc</id>
  <name>LewMC Repository</name>
  <url>https://repo.lewmc.net/{repository}</url>
</repository>
```

### For your project
If you'd like to use our repository to host your Java project, please email dev@lewmc.net to get in touch with our team.
We may be unable to accept every request, but we do consider all.