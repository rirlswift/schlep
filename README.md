# Installation instructions for Swift Artifact Gateway Prototype (schlep)

## Getting started (download the schlep client)

### Instructions for Linux or Windows (with bash)

```bash
# On local machine
mkdir -p /opt/swift/services/gateway && cd /opt/swift/services/gateway

curl https://raw.githubusercontent.com/rirlswift/schlep/master/schlep >client/schlep.sh
```

### Configure the Client Properties
```bash
# On local machine
cat >${HOME}/schlep.properties <<@
export SCHLEP_HOST=172.16.6.71
export SCHLEP_SERVICE="/opt/swift/services/gateway/server/schlep.sh"
@

```
### Add SSH configuration (to ${HOME}/.ssh/config)
```bash
Host 172.16.6.71
     HostName 172.16.6.71
     User jkadmin
     IdentityFile ~/.ssh/some-key # YOUR PRIVATE KEY -- DO NOT SHARE
     IdentitiesOnly yes
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