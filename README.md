# Butane-Schemas

Butane Schemas that helps creating [Butane](https://coreos.github.io/butane/specs/) files for [Fedora Coreos](https://getfedora.org/fr/coreos?stream=stable)

## What is it ?

This is a Json Schema that can be used as a helper to write a [butane config file](https://github.com/coreos/butane) according to [its specifications](https://github.com/coreos/butane/tree/main/docs)

## Use it with VsCode ?

- Install [vs code](https://github.com/microsoft/vscode)
- Install the [Red hat YAML extension](https://github.com/redhat-developer/vscode-yaml)
- Associate a schema in the YAML file `# yaml-language-server: $schema=<urlToTheSchema>` : [doc](https://github.com/redhat-developer/vscode-yaml#associating-a-schema-to-a-glob-pattern-via-yamlschemas)
  - For butane schema, use `# yaml-language-server: $schema=https://raw.githubusercontent.com/Relativ-IT/Butane-Schemas/Release/Butane-Schema.json"`

### How to setup vs code to associate a schema to your *.bu files whitout setting schema manually

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

:bulb: Note that files associations are optional, they only set vs code to map file type to the one it knows

## Use it with Sublime text

You can also use these butane schemas with Sublime text editor thanks to @jdoss via [sublime-butane](https://github.com/jdoss/sublime-butane)