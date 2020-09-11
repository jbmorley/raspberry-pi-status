# raspberry-pi-status

Light-weight script for determining high-level status of a Raspberry Pi

# Functionality

This script exists to allow me to monitor the temperature of my Raspberry Pi in a light-weight way. Right now the it's limited to outputting just the GPU and CPU temperatures, but I expect to add more functionality in the future when the need arises.

You're expected to use this along with cron to cat the single-line CSV output to a file for later analysis. For example, a single run of the script will produce the following output:

```csv
2020-09-10 19:23:38.321872,54.072,53.0
```

# Installation

Use with cron. For example, add something like the following to your `crontab` to record the temperature every minute:

```
*/1 * * * * /home/pi/Projects/raspberry-pi-status/raspberry-pi-status >> /home/pi/Logs/status.log
```
