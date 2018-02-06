# Packet Guardian Nagios Plugin

This Nagios plugin will check the `/api/status` endpoint of a Packet Guardian instance to
ensure the system is working correctly.

Copy the `check_packet_guardian` file to your Nagios plugins directory (by default
it's `/usr/lib/nagios/plugins`). Ensure the `requests` Python package is installed
using `pip install requests`.

## Command Flags

- `-H`: The host to check. You must include the HTTP schema (http:// or https://)
- `--user`: The username to authenticate
- `--pwd`: The password to authenticate

The user must have API read and status permissions. Meaning, the user must be in
APIRead[Only|Write]Users and APIStatusUsers.
