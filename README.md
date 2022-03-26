# Butane-Schemas

Butane Schemas that helps creating Butane files for Fedora Coreos

## What is it ?

This is a Json Schema that can be used as a helper to write a [butane config file](https://github.com/coreos/butane) according to [its specifications](https://github.com/coreos/butane/tree/main/docs)

## How to use ?

I won't describe all possibilities but the one I use :

- Install [vs code](https://github.com/microsoft/vscode)
- Install the [Red hat YAML extension](https://github.com/redhat-developer/vscode-yaml)
- Associate a schema in the YAML file `# yaml-language-server: $schema=<urlToTheSchema>`
  - for latest release, use `# yaml-language-server: $schema=https://raw.githubusercontent.com/Relativ-IT/Butane-Schemas/Release/Butane-Schema.json"` instead

## How to setup vs code to associate a schema to your *.bu files

- edit your settings.json file like :

```JSON
"settings": {
  "yaml.schemas": {
      "https://raw.githubusercontent.com/Relativ-IT/Butane-Schemas/Release/Butane-Schema.json": ["*.bu"]
  },
  "files.associations": {
    "*.bu": "yaml",
    "*.ign": "json"
  }
}
```
