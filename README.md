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
npm ci
npm run validate
npm run vsix
```

Every push to `main` and every pull request targeting `main` runs the package
workflow. The resulting `zeco-theme.vsix` is available as a GitHub Actions
artifact.

## Automated publishing

Publishing requires access to the `zeco` publisher on the Visual Studio Code
Marketplace. Add a repository Actions secret named `VSCE_PAT` containing the
Marketplace personal access token.

To publish a release:

1. Update `version` in `package.json` and `package-lock.json` with `npm run patch`
   or `npm run minor`.
2. Update `CHANGELOG.md`, commit the release changes, and push `main`.
3. Create and push a tag matching the package version exactly:

```powershell
$version = node -p "require('./package.json').version"
git tag "v$version"
git push origin "v$version"
```

The release workflow validates the tag, packages the extension, publishes that
exact VSIX to the Visual Studio Marketplace, and creates a GitHub Release with
the VSIX attached. A mismatched tag and package version stops the release.

## Author

zeco

## License

Zeco Theme is released under the [MIT License](LICENSE).
