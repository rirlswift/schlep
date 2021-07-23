# Installation instructions for Swift Artifact Gateway Prototype (schlep)

## Interactive Install Script
```bash
bash -c "$(wget -qO- https://git.io/JGVyQ)"
```

### Fully automated Installation 
```bash
bash -c "$(wget -qO- https://git.io/JGVyQ) auto"
```

## Manual Install Process (download the schlep client)

### Instructions for Linux or Windows (with bash)

```bash
# On local machine
mkdir -p /opt/swift/services/gateway/client && cd /opt/swift/services/gateway

curl https://raw.githubusercontent.com/rirlswift/schlep/master

# On Linux endpoints
chmod +x client/schlep.sh
```

### Configure the Client Properties
```bash
# On local machine

curl https://raw.githubusercontent.com/rirlswift/schlep/master/config >$HOME/schlep.properties
```
### Add SSH configuration (to ${HOME}/.ssh/config)
```bash
# On local machine

curl https://raw.githubusercontent.com/rirlswift/schlep/master/ssh >$HOME/.ssh/config.swift

# Edit and merge this file into ${HOME}/.ssh/config per your requirements.
```

### Send public key to Devops (devops@swiftengineering.com)
```bash
${HOME}/.ssh/some-key.pub # Public part of KEY -- Send to DevOps
```

## Sample commands

### Connectivity Test
```bash
/opt/swift/services/gateway/client/schlep.sh
```
### Expected output
```bash
[/tmp/schlep.Icrzxe]::Begin Query Resolution.
[/opt/swift/services/gateway/server/schlep.sh]:: Null query has been ignored.
[/tmp/schlep.Icrzxe]::End   Query Resolution.
```
