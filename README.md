---
copyright:

  years: 2018

lastupdated: "2018-07-03"

---


# Setting up the IBM Cloud Developer Tools CLI

The Developer Tools CLI is a command line approach for creating, developing, and deploying applications for developers who want to use a command line to develop end-to-end web, mobile, and microservice applications. Quickly get started with the recommended toolset by running one of the following scripts.

## Prerequisites for IBM Cloud Developer Tools

Sign up for [IBM Cloud](http://ibm.biz/ibm-registration).

*  If you're using Microsoft Windows &trade;, you must use Windows 10 or later.

* You must use the stable channel for Docker, with a minimum version of 1.13.1.

## How to Install IBM Cloud Developer Tools

To install the toolset, you can run the relevant command to start the installer. This installs the following recommended tools for IBM Cloud development (if not already installed): `Homebrew` (Mac only), `Git`, `Docker`, `Helm`, `kubectl`, `curl`, IBM Cloud CLI, IBM Cloud Developer Tools plug-in, Cloud Functions plug-in, Container Registry plug-in, Container Service plug-in, and `sdk-gen` plug-in. To install, use these installation steps:

**Mac and Linux:**

```
curl -sL https://ibm.biz/idt-installer | bash
```


**Windows 10:**

* Note: Open Windows PowerShell by right-clicking the PowerShell icon and selecting "Run as Administrator".

```
Set-ExecutionPolicy Unrestricted; iex(New-Object Net.WebClient).DownloadString('http://ibm.biz/idt-win-installer')
```

## Verify Installation
To verify installation, run the `help` command:

```
ibmcloud dev help
```

If installation was successful, the output should list usage instructions, the current version, and supported commands.

The [Reinstalling tools](/docs/troubleshoot/ts_createapps.html#appendix) section contains information to individually install all dependencies.

## Configure Your Environment

1. Connect to an API endpoint in your IBM Cloud region. For example, enter the following command to connect to the IBM Cloud US South region:

	```
	ibmcloud api https://api.ng.bluemix.net
	```

2. Log in to IBM Cloud with your IBMid.

	```
	ibmcloud login
	```

	**Note:** If your credentials are rejected, you might be using a Federated ID. Follow these steps to authenticate by using a Federated ID.

	1. Log in to [Cloud Identity and Access Management](https://www.bluemix.net/iam/#/apikeys).
	2. Select **Create API key**.
		* Enter an apiKey name and description
	3. Download your apiKey.
	4. Open the file and copy the value from the `apiKey` field.
	5. Log in using the following command:

		```
		ibmcloud login --apikey <value>
		```

3. Set your ORG and SPACE using:

	```
	ibmcloud target -o <value> -s <value>
	```

## Learn More

Now that you have your Developer Tools CLI installed, you can learn how to be effective with this powerful tool:
- [Getting Started with IDT CLI](index.html)
- [IDT (ibmcloud dev) commands](commands.html)
- [Developer Tools for VS Code](vscode.html)
- [Developer Tools for Jetbrains IDEs](jetbrains.html)

Check out the [tutorials](/docs/apps/tutorials/tutorial_bff.html) that show how to create cloud native apps that use the  Developer Tools CLI.

## Further reading

The following resources can be helpful when developing Cloud Native apps with the IBM Developer Tools CLI:

- [IBM Cloud Developer Tools main landing page](https://www.ibm.com/cloud/cli) - Main product page for IDT CLI
- [IBM Developer Tools Installer](https://github.com/IBM-Bluemix/ibm-cloud-developer-tools) - Public GitHub repo with detailed installation instructions
- [IBM Cloud App Service](https://console.bluemix.net/developer/appservice) - IBM Cloud console page, which is a companion to the IDT tools to create and manage cloud native apps
- [Report issues on GitHub](https://github.com/IBM-Cloud/ibm-cloud-developer-tools/issues)
- [IBM Cloud Tech's Slack - #developer-tools channel](https://ibm-cloud-tech.slack.com) - Request team access [here](https://slack-invite-ibm-cloud-tech.mybluemix.net/)

**Language focused**

- [Node.js on IBM Cloud](https://developer.ibm.com/node/cloud/)
- [Spring @ IBM Cloud](https://developer.ibm.com/java/spring/)
- [Swift @ IBM](https://developer.ibm.com/swift)

**Blogs and Tutorials**

- [Deploying to IBM Cloud Private with IBM Cloud Developer Tools CLI](https://www.ibm.com/blogs/bluemix/2017/09/deploying-ibm-cloud-private-ibm-cloud-developer-tools-cli/)
- [Enable existing projects for IBM Cloud with the IBM Cloud Developer Tools CLI](https://www.ibm.com/blogs/bluemix/2017/09/enable-existing-projects-ibm-cloud-ibm-cloud-developer-tools-cli/)
- [Deploying to Kubernetes on IBM Cloud with the IBM Cloud Developer Tools CLI](https://www.ibm.com/blogs/bluemix/2017/09/deploying-kubernetes-ibm-cloud-ibm-cloud-developer-tools-cli/)
