# Launch instance
`multipass launch -n <name> -c 2 -d 15G -m 4G --cloud-init kind.yaml`

# Start KIND

`multipass shell <name>`

## K8s 1.15.7
`sudo kind create cluster --name=chart-testing --wait=60s --image="kindest/node:v1.15.7@sha256:e2df133f80ef633c53c0200114fce2ed5e1f6947477dbc83261a6a921169488d"`

## K8s 1.14.10
`sudo kind create cluster --name=chart-testing --wait=60s --image="kindest/node:v1.14.10@sha256:81ae5a3237c779efc4dda43cc81c696f88a194abcc4f8fa34f86cf674aa14977"`
