# Xml Complete

This extension helps with editing XML files by providing hints.

It does not require any runtime like `java`, `python` or `xmllint`, while does partial XSD parsing.

## Features

- Basic linter (XML + partial XSD validation)

[<img src="https://raw.githubusercontent.com/rogalmic/vscode-xml-complete/gif/images/vscode-xml-complete-linter.png" width="400" style="filter: blur(1px); " title="Click to show in browser"/>](https://raw.githubusercontent.com/rogalmic/vscode-xml-complete/gif/images/vscode-xml-complete-linter.png)

- Fast autocomplete based on XSD

[<img src="https://raw.githubusercontent.com/rogalmic/vscode-xml-complete/gif/images/vscode-xml-complete-complete.png" width="400" style="filter: blur(1px); " title="Click to show in browser"/>](https://raw.githubusercontent.com/rogalmic/vscode-xml-complete/gif/images/vscode-xml-complete-complete.png)

- Formatting XML

[<img src="https://raw.githubusercontent.com/rogalmic/vscode-xml-complete/gif/images/vscode-xml-complete-format.png" width="400" style="filter: blur(1px); " title="Click to show in browser"/>](https://raw.githubusercontent.com/rogalmic/vscode-xml-complete/gif/images/vscode-xml-complete-format.png)

## Configuration

### Extension configuration per XML namespace
```javascript
"xmlComplete.schemaMapping":
[
 {
  "xmlns": "https://github.com/avaloniaui",
  "xsdUri": "https://raw.githubusercontent.com/rogalmic/vscode-xml-complete/master/test/Avalonia/AvaloniaXamlSchema.xsd"
 }
]
```
### Using `schemaLocation` attribute
```xml
<root
...
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:schemaLocation="https://raw.githubusercontent.com/rogalmic/vscode-xml-complete/master/test/Avalonia/AvaloniaXamlSchema.xsd"
/>
```

### Supported URI protocols

| Protocol  | Description                     | Example
|:---------:|:-------------------------------:|:---------------------------------:
| `data`    | XSD encoded directly in link    | `data:text/plain;base64,SGVsbG8sIFdvcmxkIQ%3D%3D`
| `file`    | XSD from local storage          | `file:///c:/windows/example.ini`
| `ftp`     | XSD from ftp server             | `ftp://ftp.kernel.org/pub/site/README`
| `http`    | XSD from http server            | `http://www.example.com/path/to/name`
| `https`   | XSD from https server           | `https://www.example.com/path/to/name`


## Known Issues

- This is a preview version, lots of bugs expected...
