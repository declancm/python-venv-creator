# virtualenv-creator

A fast and easy python virtual environment creator for Bash and PowerShell that:

- allows for python version selection after displaying currently installed versions,
- fast library installation,
- and automatic virtualenv activation.

## PowerShell Demo Video

<https://user-images.githubusercontent.com/90937622/145666970-28a7a39f-7852-4f28-a398-cee993c00f5e.mp4>

## Dependencies

- python/python3
- pip/pip3
- virtualenv

## Installation

### Bash Installation (Linux and Mac)

1. Clone the git repo:

       git clone https://github.com/declancm/virtualenv-creator.git ~/virtualenv-creator

2. Run the installation script if you wish to add the alias to your .bashrc:

       . ~/virtualenv-creator/install-bash.sh

### PowerShell Installation (Windows)

1. Clone the git repo:

       git clone https://github.com/declancm/virtualenv-creator.git $HOME\Documents\virtualenv-creator

1. Run the installation script if you wish to add the alias to your profile.ps1:

    - For PowerShell:

           pwsh /nologo -ExecutionPolicy Bypass $HOME\Documents\virtualenv-creator\install-PS.ps1

    - For Windows PowerShell

           PowerShell.exe /nologo -ExecutionPolicy Bypass $HOME\Documents\virtualenv-creator\install-WindowsPS.ps1

## Instructions

### Bash Instructions (Linux and Mac)

**If install.sh script was run:**

- Type 'pyvenv' into Bash to run the script and create a python virtualenv.

**To manually run the script:**

- Enter the following command into Bash:

      source ~/virtualenv-creator/pyvenv.sh

- This alias can be added to ~/.bashrc (if the file doesn't exist, create it),\
  to run the script with the command 'pyvenv':

      alias pyvenv='source ~/virtualenv-creator/pyvenv.sh'

### PowerShell Instructions (Windows)

_Note: Ensure powershell has the permission to run scripts so it can run it's\
own profile.ps1 script._

    Set-ExecutionPolicy -ExecutionPolicy RemoteSigned

**If install.ps1 script was run:**

- Type 'pyvenv' into PowerShell to run the script and create a python virtualenv.

**To manually run the script:**

_Note: For Windows PowerShell (the old version), replace all instances of\
'pwsh' with 'powershell'._

- Enter the following command into PowerShell:

      pwsh /nologo -ExecutionPolicy Bypass -NoExit -File $HOME\Documents\virtualenv-creator\pyvenv-PS.ps1

- An alias can be added to the location output by 'echo $profile' (if the file\
  doesn't exist, create it), to run the script with the command 'pyvenv'

      function runPyvenv { Invoke-Expression "pwsh /nologo -ExecutionPolicy `
        Bypass -NoExit -File $HOME\Documents\virtualenv-creator\pyvenv-PS.ps1" }
      Set-Alias pyvenv runPyvenv

