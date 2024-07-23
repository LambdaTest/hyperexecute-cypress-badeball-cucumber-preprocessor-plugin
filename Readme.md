## Steps to Trigger the Test

### Prerequisites

To run the Tests on HyperExecute from your Local System, you are required:

- Your LambdaTest [Username and Access key](https://www.lamdbdatest.com/support/docs/hyperexecute-how-to-get-my-username-and-access-key/)
- [HyperExecute YAML](https://www.lamdbdatest.com/support/docs/hyperexecute-yaml-version0.2/) file which contains all the necessary instructions.
- [HyperExecute CLI](https://www.lamdbdatest.com/support/docs/hyperexecute-cli-run-tests-on-hyperexecute-grid/) in order to initiate a test execution Job.
- Setup the [Environmental Variable](https://www.lamdbdatest.com/support/docs/hyperexecute-environment-variable-setup/)

### Step 1: Download or Clone the Repo
- Download or Clone this repo in order to trigger this test in your HyperExecute account.
- Go to the examples/browserify-cjs folder
```bash
cd examples/browserify-cjs
```

### Step 2: Download the CLI
Download the `HyperExecute CLI` for your OS from the links given below :

| Platform | Download Link |
| ---------| --------------------------- |
| Linux | https://downloads.lambdatest.com/hyperexecute/linux/hyperexecute |
| Windows | https://downloads.lambdatest.com/hyperexecute/windows/hyperexecute.exe |
| macOS | https://downloads.lambdatest.com/hyperexecute/darwin/hyperexecute |

### Step 3: Configure the HyperExecute YAML files
Configure your YAML file as per your use cases using **key value** pairs.

In this sample YAML file, we have mentioned:

- **version** of the YAML file
- **Timeouts** for executing your project
- **Mode of execution** is [Autosplit](https://www.lamdbdatest.com/support/docs/hyperexecute-auto-split-strategy/). You can also opt for [Matrix](https://www.lamdbdatest.com/support/docs/hyperexecute-matrix-multiplexing-strategy/) or [Hybrid](/support/docs/hyperexecute-hybrid-strategy/) mode.
- **Pre** commands in which we have to pass the installation command for all the necessary dependencies like `@badeball/cypress-cucumber-preprocessor`
- and other necessary YAML Parameters

### Step 4: Trigger the Test

> **NOTE :** In case of MacOS, if you get a permission denied warning while executing CLI, simply run **`chmod u+x ./hyperexecute`** to allow permission. In case you get a security popup, allow it from your **System Preferences** → **Security & Privacy** → **General tab**.

Run the below command in your terminal at the root folder of the project:

```bash
./hyperexecute --user YOUR_USERNAME --key YOUR_ACCESS_KEY --config RELATIVE_PATH_OF_YOUR_YAML_FILE
```