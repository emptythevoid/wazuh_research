Uses Active Response to detect and uninstall Elastic Agent.

Requirements:

On agents, local_internal_options.conf needs to have wazuh_command.remote_commands=1

remove_elastic_agent.bat needs to be deployed to "C:\Program Files (x86)\ossec-agent\active-response\bin

Note:

This active response example depends on FIM and detecting *any change* within the C:\Program Files\elastic\agent directory. This does not utilize package inventory, and does not trigger on the simple existence of this directory - only if changes occur after the baseline scan. This *should* hit shortly after, as the Elastic Agent will, at the least, modify log files.
