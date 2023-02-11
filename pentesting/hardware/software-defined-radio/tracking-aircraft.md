# Tracking Aircraft

## Summary

In this guide I will walk through the setup and installation of drivers and software required to allow a NooElec NESDR Mini 2 SDR to visually track local aircraft. &#x20;

## Driver Installation

1. Plug in the device and open Device Manager, you should see 2 devices listed similar to the picture below.

<figure><img src="../../../.gitbook/assets/image (1) (4).png" alt=""><figcaption></figcaption></figure>

2. Download and run the file [https://www.nooelec.com/store/downloads/dl/file/id/56/product/204/nesdr\_driver\_installer\_for\_windows.exe](https://www.nooelec.com/store/downloads/dl/file/id/56/product/204/nesdr\_driver\_installer\_for\_windows.exe)
3. Select 'Yes' to allow Zadig to check for application updates online.&#x20;

<figure><img src="../../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

4. Select 'Options' then 'List All Devices'

<figure><img src="../../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

5. Select the option 'Bulk-In, Interface (Interface 0)' or the correct device which may vary. Consult the driver installation documentation for further details. If the USB ID starts with 'OBDA' you have likely selected the correct device. Then click on the 'Install Driver' button.&#x20;

<figure><img src="../../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

6. You should see the 'Installing Driver' window popup.&#x20;

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

7. After a short amount of time you should see a popup to confirm the driver installation was successful.&#x20;

<figure><img src="../../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

8. If you navigate back to Device Manager you should see the device listed under 'Universal Serial Bus devices' with a driver installed.&#x20;

<figure><img src="../../../.gitbook/assets/image (2) (6).png" alt=""><figcaption></figcaption></figure>

## rtl1090 Setup

1. Download the file. [https://www.jetvision.de/manuals/rtl1090a.zip](https://www.jetvision.de/manuals/rtl1090a.zip) then extract the contents of the zip file.&#x20;
2. Download the file. [https://osmocom.org/attachments/download/2242/RelWithDebInfo.zip](https://osmocom.org/attachments/download/2242/RelWithDebInfo.zip) then extract the contents of the zip file.&#x20;
3. In the folder where you extracted the contents of the RelWithDebInfo.zip file navigate to the x32 subfolder and copy the files rtlsdr.dll & libusb-1.0.dll. Hold the ctrl key and select both files then right click and select 'copy'.

<figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

&#x20;4\. In the folder where rtl1090a.zip was extracted right click and select paste.&#x20;

<figure><img src="../../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

5. The directory should now look like the picture below.&#x20;

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

6. You can now start the rtl1090.exe file and you should see the application popup like below.&#x20;

<figure><img src="../../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

7. Click on the Start button and you should see a popup for the Windows Firewall. Click 'Allow Access' as rtl1090 opens a port and this will be required to communicate with Virtual Radar later.&#x20;

<figure><img src="../../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

8. You should see that the rtl1090 application is receiving data if your aerial is connected and you are within range of aircraft.&#x20;

<figure><img src="../../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

## Virtual Radar Setup

1. Download and run the file [https://www.virtualradarserver.co.uk/Files/VirtualRadarSetup.exe](https://www.virtualradarserver.co.uk/Files/VirtualRadarSetup.exe)
2. Accept the agreement and click 'Next'.&#x20;

<figure><img src="../../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

3. Click 'Next' again.&#x20;

<figure><img src="../../../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure>

4. Click 'Next' again.&#x20;

<figure><img src="../../../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>

5. Leave the port as the default option of '80' and click 'Next'.&#x20;

<figure><img src="../../../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure>

6. Click 'Next' to accept the default option.&#x20;

<figure><img src="../../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

7. This option is only required if other computer on the same network need to access Virtual Radar. Unless you specifically require this it's best to leave it unchecked.&#x20;

<figure><img src="../../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

8. Select 'Install'.&#x20;

<figure><img src="../../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

9. Select 'Finish' to complete installation.&#x20;

<figure><img src="../../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

10. Click on the Start menu and then select 'Virtual Radar'

<figure><img src="../../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

11. Select 'Download and install this feature' if you are prompted.&#x20;

<figure><img src="../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

12. Click 'Close' once done.&#x20;

<figure><img src="../../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

13. If '.NET Framework 3.5 (includes .NET 2.0 and 3.0)' was required to be installed. You may have to start Virtual Radar from the Start Menu again.&#x20;
14. Once Virtual Radar has loaded select 'Tools' then 'Options'.&#x20;

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

15. Select 'Receivers' -> 'Receiver'.&#x20;

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

16. Change the Format option to be 'AVR or Beast Raw Feed'. Also change the Port option to be '31001'.&#x20;

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

17. Click on the 'Test Connection' button and you should see a popup like the one below indicating that the connection was successful.&#x20;

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

18. Click 'OK' to close the options.&#x20;

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

19. You should now see the number in the 'Feed status' section changing indicating that the rtl1090 program is sending data to Virtual Radar.&#x20;

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

20. Click on the link highlighted below to view the map.&#x20;

<figure><img src="../../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

21. The map seems to default to Heathrow Airport in the United Kingdom so you may have to navigate on the map to your location.&#x20;

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

22. &#x20;If there are aircraft in range you should see them visually plotted on the map.&#x20;

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>
