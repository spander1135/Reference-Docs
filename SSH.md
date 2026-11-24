# Secure Shell (SSH) SOPs

### Start the agent
``` bash
eval "$(ssh-agent -s)"
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

### Check SSH Configuration
``` bash
cat ~/.ssh/config
```

### Test SSH Connection and Authentication with GitHub
``` bash
ssh -T git@github.com
```

### Generate New ED25519 SSH Key Pair
``` bash
ssh-keygen -t ed25519 -C "email@address.com" -f ~/.ssh/id_ed25519
```
