# Language Files

Language files are used in Essence to serve messages to players

These are automatically updated whenever you update your plugin.

We currently only support en-gb, you can see a [template here](https://github.com/lewmilburn/Essence/blob/main/src/main/resources/language/en-gb.yml) if you'd like to create a translation. If you have created a translation and would like to add it to Essence please open an issue on our [GitHub](https://github.com/lewmc/essence), thank you.

## Creating a new language file.
> Essence may require restarting after changing the file it uses to grab messages, if you're editing a file that is already set as active in config, no restart is required.

1. Create a new .yml file in the /plugins/essence/languages folder. You should give it a unique name such as custom.yml
2. Copy the contents of en-gb.yml to this file.
3. Customise any messages you wish to.
4. Change the language option in config.yml to the name of your file without the yml ending (e.g. "custom").