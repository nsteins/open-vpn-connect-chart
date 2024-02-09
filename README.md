# open-vpn-connect-chart
A Helm chart for setting up OpenVPN connection for your cluster.

### Instructions
- download your .ovpn client configuration file, and put it in this directory, renamed to `client.ovpn`
- create a file called `auth.txt` in the root directory containing your certificate password
- edit `client.ovpn` to add the line `askpass /vpn/auth.txt` after `auth-nocache`
- Check if helm is installed, otherwise install (`brew install helm`)
- Making sure that you are pointed at your local cluster (`k8s local`), install the helm configuration with `helm install . --generate-name`

If you have an error and need to update, you must first delete the old helm installs. Use `helm list` and `helm delete`.
