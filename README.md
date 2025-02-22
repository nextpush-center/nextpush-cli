# NextPush Command Line Interface (CLI)

NextPush CLI is a command-line tool for managing NextPush, a custom CodePush server.
Our goal is to provide developers with an easy-to-use and powerful interface for handling over-the-air (OTA) updates efficiently.
With NextPush CLI, you can authenticate, manage your apps, deploy updates, and configure your projects—all from the terminal.

We are forking this project from [code-push-server](https://github.com/microsoft/code-push-server/tree/main/cli) and will continue to maintain it.

## Prerequisites
- Node.js 18 or higher version
- NextPush Account. You can create an account at [NextPush](https://nextpush.center)



## Installation

```bash
npm install -g nextpush-cli
```

## Usage

```
$ nextpush --help

.__   __.  __________   ___ .___________.  .______    __    __       _______. __    __
|  \ |  | |   ____\  \ /  / |           |  |   _  \  |  |  |  |     /       ||  |  |  |
|   \|  | |  |__   \  V  /  `---|  |----`  |  |_)  | |  |  |  |    |   (----`|  |__|  |
|  . `  | |   __|   >   <       |  |       |   ___/  |  |  |  |     \   \    |   __   |
|  |\   | |  |____ /  .  \      |  |       |  |      |  `--'  | .----)   |   |  |  |  |
|__| \__| |_______/__/ \__\     |__|       | _|       \______/  |_______/    |__|  |__|     CLI v1.0.0
=======================================================================================

NextPush is a service that enables you to deploy mobile app updates directly to your users' devices.
visit https://nextpush.center/ for more information

Usage: nextpush <command>

Commands:
  nextpush migrate        Import all your applications, CodePush versions, and metrics from App Center with a single command using your API key
  nextpush access-key     View and manage the access keys associated with your account
  nextpush app            View and manage your NextPush apps
  nextpush collaborator   View and manage app collaborators
  nextpush debug          View the NextPush debug logs for a running app
  nextpush deployment     View and manage your app deployments
  nextpush login          Authenticate with the NextPush server in order to begin managing your apps
  nextpush logout         Log out of the current session
  nextpush patch          Update the metadata for an existing release
  nextpush promote        Promote the latest release from one app deployment to another
  nextpush register       Register a new NextPush account
  nextpush release        Release an update to an app deployment
  nextpush release-react  Release a React Native update to an app deployment
  nextpush rollback       Rollback the latest release for an app deployment
  nextpush session        View and manage the current login sessions associated with your account
  nextpush whoami         Display the account info for the current login session
```

You can get more information about the commands and options by running:

```bash
nextpush <command> --help
```


## Migrating from Appcenter to NextPush

Import all your applications, CodePush versions, and metrics from App Center with a single command using your API key—no need to manually create each application.

This ensures:
- Your deployment key and other important keys remain unchanged.
- Your application names stay the same.
- All your versions are migrated.
- All your statistics and analytics are transferred to NextPush.

✅ With just one command! Yes, with a single command, you can pick up right where you left off. 

### Step 1: Create a NextPush account

If you don't have a NextPush account, you can create one at [NextPush](https://nextpush.center).

### Step 2: Get your App Center API key

- You can get your App Center API key from [here](https://appcenter.ms/settings/apitokens/create).
- Set Description as "nextpush" and select "Read Only" access. Then click "Add new API token"
- Copy the generated API key

### Step 3: Run the migration command

```bash
nextpush migrate --api-key your-appcenter-api-key
```

### Important Notes

- Only applications you own will be imported. If you are an organization member, please use the organization owner's API key.
- You can perform this import process multiple times with different API keys.   
- Applications with names that already exist in your account will not be imported.


## Issues

If you encounter any issues, please feel free to open an issue on [GitHub](https://github.com/nextpush-center/nextpush-cli/issues).