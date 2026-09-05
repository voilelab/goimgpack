# goimgpack

![License](https://img.shields.io/github/license/voilelab/goimgpack)
![Go Version](https://img.shields.io/github/go-mod/go-version/voilelab/goimgpack)
![Comic Book Archive](https://img.shields.io/badge/CBZ-Support-blue)
![PDF](https://img.shields.io/badge/PDF-Support-blue)

A simple image packer for combining multiple images into a single file.

![Preview](./preview.png)

## Features

### Export Formats
- Single Image: PNG, JPEG, WebP, GIF, BMP, TIFF
- Multiple Images: ZIP, CBZ, PDF

### Import Formats
- Images: PNG, JPEG, WebP, GIF, BMP, TIFF
- Images in archives: ZIP, CBZ
- Images in PDF
- Images in directories (non-recursive)

### Operations
- Add images
- Duplicate a single image
- Remove a single image
- Reorder a single image
- Save a single image
- Rotate a single image
- Cut a single image into halves

## Packaging the App for Desktop

To package the app for macOS, use the following command:

```bash
fyne package -os darwin
```

## Releasing

`FyneApp.toml`'s `Version` is the single source of truth for the released version.

1. Run the **Prepare release** workflow on `main` and enter the new version (e.g. `0.6.0`).
   It opens a PR that bumps `FyneApp.toml`.
2. Merge that PR. **Release** picks up the version change on `main`, tags `v0.6.0`,
   builds Windows / Linux / macOS packages and publishes the GitHub Release.

A version with a suffix (e.g. `0.6.0-rc1`) is published as a pre-release. Pushes to
`main` that leave the version untouched release nothing, so re-runs are safe.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
