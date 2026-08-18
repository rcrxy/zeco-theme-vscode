# Zeco Theme

A carefully tuned dark color theme for Visual Studio Code, created by **zeco**.

## Features

- Balanced contrast for UI and code editor
- Custom bracket highlights and gutter colors
- TextMate and semantic token colors
- Tuned for long coding sessions

## Installation

### Visual Studio Code Marketplace

1. Open the Extensions view in Visual Studio Code.
2. Search for **Zeco Theme**.
3. Install the extension.
4. Select **Zeco Theme Dark** from the Color Theme picker.

### VSIX package

1. Press `Ctrl+Shift+P` and run `Extensions: Install from VSIX...`.
2. Choose the packaged `.vsix` file.
3. Select **Zeco Theme Dark** from the Color Theme picker.

## Development

- Update `themes/dark.json` to adjust theme colors.
- Update `package.json` metadata before each release.
- Record user-visible changes in `CHANGELOG.md`.

## Packaging

```powershell
npx --no-install vsce package
```

## Publishing

Publishing requires access to the `zeco` publisher on the Visual Studio Code Marketplace.

```powershell
npx --no-install vsce login zeco
npx --no-install vsce publish
```

## Author

zeco

## License

Zeco Theme is released under the [MIT License](LICENSE).
