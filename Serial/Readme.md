# Add RFID/NFC read and write to your Pi 

### Step One: Run raspi-conf
From the command prompt enter the following command:
`
sudo raspi-config
`

### Step Two: Disable Serial Console
From the main menu, select **option 7 (Serial)**, then **select 'No'** to disable shell and kernel messages via UART.

### Step Three: Enable UART
On the latest Jessie Raspbian, you may also need to enable the UART for user usage! Edit config.txt with 
`
sudo nano /boot/config.txt
`
and remove the line
`
enable_uart=0
`
if it exists. And add at the end of the file
`
enable_uart=1
`
Save the file

### Lastly: Reset
From the command prompt enter the following commands to reboot your Raspberry Pi board, freeing UART up in the process:
`
sudo reboot
`

# Building libnfc

### Step One: Download libnfc
Before you can do anything, you will need to get a copy of libnfc. Make sure you have an Ethernet cable connected to your Pi, and run the following commands to get libnfc 1.7.0
