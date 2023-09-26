# Helper script for SNO with Assisted Installer in Hetzner servers
Use this script to deploy [Single Node OpenShift](https://docs.openshift.com/container-platform/4.13/installing/installing_sno/install-sno-installing-sno.html) 
(SNO) clusters using [Assisted Installer](https://console.redhat.com/openshift/assisted-installer/clusters/) 
in Hetzner servers.

This script requires a configuration files that must be placed in a
directory. You can have different directories for different servers
and/or installations.

Use the placeholder files in the `sno/` directory to fill them with
your own data and invoke the script with the name of the directory:

```bash
./new-cluster sno
```

WARNING: This is a WIP project. I don't know if I'll ever finish or
improve it more than it's now as it works for me. If might fail and
you're expected to have some knowledge to troubleshoot the
installation.

Pull requests are welcome!
