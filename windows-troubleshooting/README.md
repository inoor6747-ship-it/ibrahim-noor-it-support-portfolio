# Windows Connectivity Failure

## Problem
User connected to Wi-Fi but could not access any websites.

## Investigation
Checked IP configuration using:
ipconfig

Result showed APIPA address (169.254.x.x)

Tested gateway:
ping 192.168.1.1 → failed

## Root Cause
DHCP lease was not assigned.

## Resolution
Released and renewed IP:
ipconfig /release
ipconfig /renew

System obtained valid IP and connectivity restored.

## Prevention
Verify DHCP service and adapter settings before escalation.
