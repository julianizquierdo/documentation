---
date: 2018-01-01
title: Installation Guide
description: Step-by-step guide to installing the SDK
redirect_from:
  - /documentation/installation-guide/
categories:
  - getting-started
type: Document
set: getting-started
set_order: 2
---

To build scenes for Decentraland you will need to install the Command Line Interface (CLI).

The CLI allows you to compile and preview your scene in an "off-chain" development environment. After testing your scene locally, you can use the CLI to upload your content to the content server, linking it with your LAND.

**Please note:** Currently, the Decentraland SDK (bundled with the CLI installation) only supports TypeScript.

The Decentraland CLI is distributed via [npm](https://www.npmjs.com/get-npm?utm_source=house&utm_medium=homepage&utm_campaign=free%20orgs&utm_term=Install%20npm).

## Before you Begin

Please install the following dependencies before you install the CLI:

- [Node.js](nodejs.org) (version 8 or later)

## Install the CLI

Open the _Terminal_ app and run the following command:

```bash
npm install -g decentraland
```

Once the installation is complete, the `dcl` command will be globally available.


## Update the CLI on any platform

To update the CLI to the latest supported version, we recommend first uninstalling the CLI and then reinstalling a fresh version. To do this, run the following commands:

```bash
// uninstall
npm rm decentraland -g

// install
npm install -g decentraland
```

#### Update the SDK version of a scene

If your CLI is up to date, the new projects you create with it will use the latest version of the SDK.

The SDK version used by your existing projects doesn't change by updating the CLI. You need to manually update the SDK version in the projects.

Run the following command on the scene folder:

```bash
npm i decentraland-ecs@latest
```

You can confirm that it worked by checking the `package.json` file for the scene, and looking for the `decentraland-ecs` version there.

<!--


To update the version of the Decentraland SDK used by a project:

1.  Open the file `package.json` in the project folder.
2.  In this file, look for the field `decentraland-ecs`:

    * If the value is `latest`, keep it.
    * If the version points to a number or a build that isn't the latest version of the SDK, change it to `latest`.
    * If you can't find the field `decentraland-ecs`, but do find the field `decentraland-api`, then your project is written with a deprecated version that's older than `5.0`. Create a new project with the CLI and [migrate the content manually](https://decentraland.org/blog/tutorials/sdk-migration/) to it.

3. Delete the file `package-lock.json` and the folder `node-modules` from the project.
4. Run the scene preview with `dcl start`. All the dependencies should be automatically reinstalled, according to the versions listed in `package.json`.





#### Optional: Install Git

Mac OS and linux-based machines should have git installed by default, these steps should only be relevant to Windows based machines.

1.  Download [git](https://git-scm.com/download/win) (you'll likely want the 64-bit Windows version)
2.  The installation process will prompt you to choose severla options, we recommend the following:
	1.  Install **git bash**
	2.  For default text editor, select **Use the Nano editor by default**
	3.  For path environment, select **Use Git from the Windows Command Prompt**
	4.  For SSH executable, select **Use OpenSSH**
	5.  For HTTPS transport backend, select **Use the OpenSSL library**
	6.  For line ending conversions, select **Checkout Windows-style, commit Unix-style line endings**
	7.  For the terminal emulator to use with Git Bash select **Use MinTTY**
	8.  On the final installation screen select the following options
		- **Enable file system caching**
		- **Enable Git Credential Manager**
		- **Enable symbolic links**

-->