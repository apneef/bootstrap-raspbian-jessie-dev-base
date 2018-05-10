# Raspbian Jessie: Build Base for Lightweight Development Environments

For general information about this repo and related ones, please see [Provision Lightweight Development Environments](http://github.com/neopragma/provision-lightweight-development-environments).

## From -> To

**From:** No operating system installed.

**To:** Raspbian Jessie configured to receive provisioning to customize it for software development.

### 1. Assemble a Raspberry Pi 

Follow the instructions at <a href="https://www.raspberrypi.org">RaspberryPi.org</a> and/or the instructions that came with your kit and/or the guide <a href="pi-assembly.md">in this repo</a>.

### 2. Install operating system

Booting from the micro-SD, the Pi will display the New Out of Box Software (NOOBS) menu listing several operating systems available to install. The simplest thing to do is to choose the default Raspbian desktop OS. It will run a while and install itself.

### 3. Set system preferences

It comes up by default into the lxde-pi graphical desktop environment as user 'pi'. Choose the raspberry-shaped icon on the menu bar and select "Preferences..." from the drop-down menu, and then "Raspberry Pi Configuration."

#### On the System tab:

- Set a password
- Set a hostname
- Choose the auto login option you want. For a single-user lightweight development environment, I suggest auto login to a command prompt.

#### On the Interfaces tab:

- Set "SSH" to "Enable"

#### On the Localisation tab:

- Choose "Locale" and set your language, country, and character set. I suggest "UTF-8" for character set.
- Choose "Timezone" and set your area and location.
- Choose "Keyboard" and select your keyboard preference. Note: If you're using US English, I suggest Variant "English (US, with euro on 5)". Other settings result in strange (wrong) characters for some keys.
- Choose "Set WiFi Country" and select your country from the list.

### 4. Download and run provisioning script

Raspbian comes with git already installed. Run the following command to download the provisioning script:

```shell
cd
git clone git://github.com/neopragma/bootstrap-raspbian-jessie-dev-base.git
```

Change to the bootstrap directory and run the bootstrap script. The bootstrap script does the following:

- Updates the operating system, in case new software was issued subsequent to the creation of the installer
- Creates directory ~/bin
- Prepends directory ~/bin to the PATH (appends an export to the end of ~/.bashrc)
<li>Copies a script named 'gui' into ~/bin that starts X sessions with a selected window manager
- Installs the NeoVim editor, several plugins, and several configuration files.

```shell
cd bootstrap-raspbian-jessie-dev-base
./bootstrap
```

After the bootstrap script completes successfully, your Pi is provisioned as the base for a software development environment. However, no specific language support has been added to NeoVim at this point. You know which languages you will work with, so you will have to look for the compilers, dependency managers, and NeoVim plugins you require.

