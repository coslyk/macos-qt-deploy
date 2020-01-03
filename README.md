# macos-qt-deploy
Deploys the Qt Application under macOS, also deploys the Homebrewed libraries

## Why this tool?
Qt's `macdeployqt` tool bundles Qt and other libraries to the App, but it doesn't change the dependency paths. The libraries still use absolute path to refer dependencies, which makes the App fail to run on other computers.

This script calls `macdeployqt` first, then it scan all the bundled homebrewed libraries and change their absolute path to the relative one.

## Usage
```
./deploy.sh path/to/Program.app
```
