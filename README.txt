If you're developing on Ubuntu Linux, you need to add a udev rules file that contains a USB configuration for each type of device you want to use for development. In the rules file, each device manufacturer is identified by a unique vendor ID, as specified by the ATTR{idVendor} property. For a list of vendor IDs, see USB Vendor IDs, below. To set up device detection on Ubuntu Linux:
Log in as root and create this file: /etc/udev/rules.d/51-android.rules.
Use this format to add each vendor to the file:
SUBSYSTEM=="usb", ATTR{idVendor}=="0bb4", MODE="0666", GROUP="plugdev" 

In this example, the vendor ID is for HTC. The MODE assignment specifies read/write permissions, and GROUP defines which Unix group owns the device node.
Note: The rule syntax may vary slightly depending on your environment. Consult the udev documentation for your system as needed. For an overview of rule syntax, see this guide to writing udev rules.
Now execute:
chmod a+r /etc/udev/rules.d/51-android.rules

When plugged in over USB, can verify that your device is connected by executing adb devices from your SDK platform-tools/ directory. If connected, you'll see the device name listed as a "device."
