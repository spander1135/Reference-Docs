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
