# SafeRM - Safer Recursive File Deletion

SafeRM is a custom shell script that provides an extra layer of protection when using the `rm -rf` command. It prompts the user for confirmation before deleting files and directories, helping to prevent accidental data loss.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Supported Scenarios](#supported-scenarios)
- [License](#license)

## Installation

#### To use SafeRM, follow these installation steps manually:

1. Copy the `saferm` file to the `/usr/local/bin` directory.
2. `chmod +x /usr/local/bin/saferm`
3. Edit the `~/.bashrc` file, add an alias for `rm` as follows:   
`alias rm='/usr/local/bin/saferm'`
4. `source ~/.bashrc`  
#### or use the following cURL or Wget command:  
```shell
curl -o /usr/local/bin/saferm https://raw.githubusercontent.com/kookob/safe-rm/master/saferm && sudo chmod +x /usr/local/bin/saferm && echo "alias rm='/usr/local/bin/saferm'" >> ~/.bashrc && source ~/.bashrc
```
```shell
wget -P /usr/local/bin https://raw.githubusercontent.com/kookob/safe-rm/master/saferm && sudo chmod +x /usr/local/bin/saferm && sudo echo "alias rm='/usr/local/bin/saferm'" >> ~/.bashrc && source ~/.bashrc
```

## Usage
#### Verify the `saferm` command:  
`rm -rf safermTest`  
If you see the following content, it means `rm -rf /` to prevent accidental deletion has taken effect.
   ```shell
   Danger: Are you sure you want to delete everything? (yes/no): 
   no
   Deletion canceled.
   ```

## Supported Scenarios
- rm -rf /
- rm -rf /*
- rm -rf * (root directory)
- rm -rf ./* (root directory)

## License
MIT
