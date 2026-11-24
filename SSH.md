# Secure Shell (SSH) SOPs

### Start the agent
``` bash
eval "$(ssh-agent -s)"
```

### Check SSH Configuration
``` bash
cat ~/.ssh/config
```

### Check for Existing ED25519 File
``` bash
# Check all files
ls -la ~/.ssh

# Check for specific file
ls -la ~/.ssh/id_ed25519*
```

### Generate New ED25519 SSH Key Pair
``` bash
ssh-keygen -t ed25519 -C "email@address.com" -f ~/.ssh/id_ed25519
```

### Add SSH key
``` bash
# root location
ssh-add ~/.ssh/id_ed25519

# Custom Location and Name
ssh-add C:/root-folder/.ssh/id_ed25519_personal
```

### Print public key to terminal
``` bash
# Print key to terminal
cat ~/.ssh/id_ed25519

# Clip key directly to clipboard
cat ~/.ssh/id_ed25519.pub | clip
```

### Test SSH Connection and Authentication with GitHub
``` bash
ssh -T git@github.com
```

### Additional Information
``` bash
# Append --help to desired command
ssh-keygen --help
ssh-add --help
```

Command | Flag | Meaning
--- | --- | ---
`ssh-add` | `-l` | List fingerprints of all keys currently loaded int he SSH agent
`ssh` | `-T` | Disable pseudo-terminal allocation (used when testing GitHub auth)
`ssh-keygen` | `-t` | Type of key algorithm to create (e.g., `ed25519` or `rsa`)
`ssh-keygen` | `-C` | Comment/label added to the end of the public key (e.g., your email)
`ssh-keygen` | `-f` | Filename and path where the generated key files should be saved
`ls` | `-l` | Long format (shows file permissions, sizes, and dates)
`ls` | `-a` | All files, including hidden files starting with a dot (`.`)
