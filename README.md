# SafeRM - Safer Recursive File Deletion

SafeRM is a custom shell script that provides an extra layer of protection when using the `rm -rf` command. It prompts the user for confirmation before deleting files and directories, helping to prevent accidental data loss.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Installation

To use SafeRM, follow these installation steps:

1. Copy the `saferm` file to the `/usr/local/bin` directory.
2. `chmod +x /usr/local/bin/saferm`
3. Edit the `~/.bashrc` file, add an alias for `rm` as follows:   
`alias rm='/usr/local/bin/saferm'`
4. `source ~/.bashrc`

## Usage
1. Create the directory "/safermTestDir" for verification:  
`mkdir /safermTestDir`
2. Verify the `rm` command:  
`rm -rf /safermTestDir`  
If you see the following content, it means `rm -rf /` to prevent accidental deletion has taken effect.
   ```shell
   Danger: Are you sure you want to delete everything? (yes/no): 
   no
   Deletion canceled.
   ```
3. Finish

## License
MIT
