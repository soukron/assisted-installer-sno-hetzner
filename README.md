# Helper script for SNO with Assisted Installer in Hetzner servers
WARNING: This is neither supported nor endorsed by Red Hat or Hetzner. It is experimental and not intended for production use. Use it under your own risk.

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

Requirements:
- [Assisted Installer Token](https://access.redhat.com/documentation/en-us/assisted_installer_for_openshift_container_platform/2023/html/assisted_installer_for_openshift_container_platform/installing-with-api#installing-the-openshift-cluster-manager-cli_installing-with-api).
- Hetzner webservice credentials. Login in Robot, click on the user icon in the upper right corner and then on "Settings" and "Webservice and app settings".
- Server ID.
- Server Hostname/IP address.

What it does:
- Creates the required items using Assisted Installer API
- Enables rescue mode and reboots the server using Hetzner API
- Copies the files to the server and reboots the server using [Pablo Alonso's](https://github.com/palonsoro/hetzner-sno-provision-host) script.
- Starts the SNO installation using Assisted Installer API

What it doesn't do:
- Error handling
- Waits for the installation to complete

WARNING: This is a WIP project. I don't know if I'll ever finish or
improve it more than it's now as it works for me. If might fail and
you're expected to have some knowledge to troubleshoot the
installation.

Pull requests are welcome!
