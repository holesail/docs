# 📪 Install through npm (Recommended)

Holesail is available through npm, which is the recommended way to install and use It currently. All the latest updates, patches, and bug fixes are first applied to the npm package and then to everything else.

## Step 1- Install Nodejs

Holesail needs at least Nodejs version 16 >= or above to run. On Linux or Mac, you can use [NVM](https://github.com/nvm-sh/nvm) to install Nodejs.

Run the following command to install the Node version manager:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

Add nvm to the environment variable:

```bash
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

Close and reopen the terminal to install Nodejs 20:

```bash
nvm install 20
nvm use 20
```

### Install Nodejs Windows

You can install Nodejs on Windows by downloading a prebuilt installer from [here](https://nodejs.org/en/download/prebuilt-installer/current).&#x20;

## Step 2- Install Holesail through npm

Once you have the latest Node version installed, you can run the following commands to install Holesail.

**On Linux:**

```bash
sudo npm i holesail -g
```

**On Mac:**

```bash
npm i holesail -g
```

On Windows, open **command prompt** and type:

```bash
npm i holesail -g
```

If your installation fails on Windows, try running the command prompt instead of Powershell or Terminal. You can also try enabling third-party script execution by launching Powershell as Administrator and running:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
```

## Step 3 - Verify Installation

Run the following command, if it returns an output then holesail is installed on your system:

```bash
holesail --help
```

You are now all set to set sail with holesail.
