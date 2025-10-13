Example of using Wazuh to identify connection of a Flipper Zero on Windows and disabling it using an Active Response.

Requirements and Limitations:

Requires the group policy "Audit Pnp" be enabled. This allows triggering new device detection in Wazuh's syscollector

Requires agents to have local_internal_options.conf set to allow wazuh_command.remote_commands=1

Assumes we know the device ID of the device and it hasn't been changed

Because it performs actions based purely on VID and PID (rather than Instance ID) when calling pnputil during active response, this method will only work on Windows 11 due to changes in pnputil
