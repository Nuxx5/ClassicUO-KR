# macOS build

The `Build macOS` GitHub Actions workflow publishes runnable macOS app bundles
for Intel (`osx-x64`) and Apple Silicon (`osx-arm64`) using native AOT and the
FNA dependencies from upstream ClassicUO. The KR asset project is already
referenced by `ClassicUO.Assets`, so those KR-specific asset readers are part of
the client build.

Run it from **Actions → Build macOS → Run workflow**, or push to `main`. The
workflow uploads one zip artifact per architecture. Extract the zip and move
the `.app` to Applications. These are unsigned builds; Gatekeeper may require
the user to allow the app to run.

