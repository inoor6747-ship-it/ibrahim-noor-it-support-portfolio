# Ticket: Unable to Print to Office Printer

## User Report
User states printer shows online but documents stay in queue and never print.

---

## Investigation

1. Verified printer status
Printer reachable on network (ping successful)

2. Checked print queue
Multiple stuck jobs observed

3. Restarted Print Spooler service
services.msc → Print Spooler → Restarted

Jobs still stuck

4. Checked driver
Driver mismatch after Windows update

---

## Root Cause
Incorrect printer driver caused spooler to hold jobs indefinitely.

---

## Resolution
Removed printer → Reinstalled correct manufacturer driver → Reconnected via IP address

Printing successful ✔

---

## Prevention
After Windows updates, verify shared printer drivers remain compatible.

