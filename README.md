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