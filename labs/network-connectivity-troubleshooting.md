# Network Connectivity Troubleshooting

## Purpose

A basic training checklist for investigating a computer that cannot connect to the network.

## Troubleshooting Steps

1. **Check the physical connection**
   - Confirm the Ethernet cable is connected securely.
   - Check for link lights on the computer and network device, if available.
   - If using Wi-Fi, confirm Wi-Fi is enabled and Airplane mode is off.

2. **Check the connection status**
   - Open Windows network settings.
   - Confirm whether the computer shows an active Ethernet or Wi-Fi connection.
   - Check whether other devices can connect to the same network.

3. **Review IP configuration**
   - Open Command Prompt and run:
     ```cmd
     ipconfig
     ```
   - Review the network adapter, IPv4 address, default gateway, and DNS servers.
   - An address beginning with `169.254` can indicate that the computer did not receive an address from DHCP.

4. **Test connectivity**
   - Test the local network gateway:
     ```cmd
     ping <default-gateway>
     ```
   - Test an external IP address:
     ```cmd
     ping 8.8.8.8
     ```
   - Test DNS name resolution:
     ```cmd
     nslookup example.com
     ```

5. **Apply basic checks**
   - Disconnect and reconnect to Wi-Fi, or reseat the Ethernet cable.
   - Restart the computer if appropriate.
   - If authorized, renew the IP address:
     ```cmd
     ipconfig /release
     ipconfig /renew
     ```
   - Record any error messages and the results of each check.

## Interpreting Results

- If the gateway cannot be reached, check the local connection, adapter, cable, or Wi-Fi.
- If the gateway responds but an external IP does not, the issue may be beyond the local network.
- If an external IP responds but a domain name does not, check DNS settings or DNS resolution.

## Training Note

This file documents a basic troubleshooting procedure for learning purposes. Commands and network changes should only be used on a device and network you are authorized to troubleshoot.
