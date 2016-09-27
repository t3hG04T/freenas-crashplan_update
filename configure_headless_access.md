## General CP info
https://support.code42.com/CrashPlan/4/Configuring/Using_CrashPlan_On_A_Headless_Computer

# Copy headless access token
```sh
cat /var/lib/crashplan/.ui_info
```

# Paste info client PC info
For user-only install:
```
C:\Users\{USER}\AppData\Local\CrashPlan\.ui_info
```
Make file read-only to prevent overwrites!

# Change local listening port

Change the port in .ui_info on **local machine** to 4200.

# Tunnel the ports via SSH (Putty)

Add a port tunelling from **4200** local to port: **localhost:4243**.

**WARNING: The port has to match the listening port on the headless machine.**

_In my case it meant tunelling to port 4541 for some reason_. If the ports don't match Crashplan GUI won't be able to connect correctly.

# Launch GUI and configure away!
