# LewMC Wiki

You're here! This is the LewMC Wiki, it's the source of all the information you could need about all things LewMC!

## Contributing
Our Wiki runs on JetBrains Writerside.
Please note that whilst it uses markdown files, it's actually using a custom version of Semantic Markup.
This means it uses all the standard markup stuff we know and love, with some extra bits that look somewhat like HTML. 

You don't need to know how to use all the fancy stuff as standard markup is just fine, but if you'd like to
you can [learn more on the JetBrains website](https://www.jetbrains.com/help/writerside/markup-reference.html).

### Branches
We organise changes into branches for upcoming versions of software.
If you're making changes for existing versions you can do these in `main`, but if you're helping to document future versions please do so in the relevant branch.
For example, ES-1.9.0 refers to Essence version 1.9.0 which at the time of writing was the version in development.

![LewMC Wiki Contributing - Branches](LewMC Wiki Contributing - Branches.png)

### Codes
Each topic is assigned a two-letter code, branches and pages must have the code as a prefix to help us organise things.

| Software          | Code |
|-------------------|------|
| Essence           | ES   |
| Kryptonite        | KR   |
| Jailhouse         | JH   |
| Galactica         | GA   |
| Lew's Client Pack | LP   |
| SimplyAesthetic   | SA   |

See the Style Guide below for more information on page naming.

## How to edit the Wiki
### Existing pages
If you'd like to contribute to existing pages you can edit the files directly on GitHub or in Writerside.

To edit on GitHub [navigate to the repository](https://github.com/LewMC/Wiki) then enter the `/Writerside/topics` directory.

You'll now see a number of files that correspond to Wiki pages,

### New pages and content

## Style Guide
### Page names and URLs
Page names should follow a typical guide such as this:

The main pages for each topic should be the topic's name, then each subpage should contain the coded prefix. An example is shown below for Essence.

![Essence's pages on GitHub.](Essences pages on GitHub.png)

This also allows our URLs to be uniform, since Writerside doesn't translate pages to /essence/commands for example, it instead uses /es-commands, allowing our visitors to know what software they're looking for easily.

We also like our pages to follow a similar structure across topics.

```
Changelogs
Configuration
Commands
Features
 \ Pages telling users how to use each feature
System Requirements
Troubleshooting
Any other pages
```

These pages can also have subpages, and other pages can be added on after this set.
If certain pages aren't required (for example modpacks might not need a commands page) they can be omitted.