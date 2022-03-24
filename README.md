# Acer-XC-885-EFI
Opencore Hackintosh EFI for Acer-XC-885
Processor: i5-8400
RAM : 2x 8GB DDR4 2666mhz
Graphics: iGPU UHD 630
Wifi/BT : BCM94360CS2
SSD: NVME Phison PM8512GPTCB4B8TF
OS: macOS Monterey 12.3

Currently, this hack works well with VGA Port (and monitor) as it can wake up from sleep. It does boot up with HDMI Port (and monitor) as well but it cannot wake up from sleep. 

With Monterey, boot times have been slowed and the quick fix for now is to change Kernel > Quirks > SetApfsTrimTimeout from -1 to 0. The specific issue is in [this thread](https://www.reddit.com/r/hackintosh/comments/tj0z7t/tx_flush_750_for_macos_monterey_oc_075/) and you can read more about the [fix here](https://www.reddit.com/r/hackintosh/comments/sfqhcc/comment/i1eqqkg/?utm_source=share&utm_medium=web2x&context=3). 




Please change MLB, SystemSerialNumber, SystemUUID into your code:

```
		<dict>
			<key>AdviseFeatures</key>
			<false/>
			<key>MLB</key>
			<string>EDIT THIS</string>
			<key>MaxBIOSVersion</key>
			<false/>
			<key>ProcessorType</key>
			<integer>0</integer>
			<key>ROM</key>
			<data>
			ESIzRFVm
			</data>
			<key>SpoofVendor</key>
			<true/>
			<key>SystemMemoryStatus</key>
			<string>Auto</string>
			<key>SystemProductName</key>
			<string>Macmini8,1</string>
			<key>SystemSerialNumber</key>
			<string>EDIT THIS</string>
			<key>SystemUUID</key>
			<string>EDIT THIS</string>
		</dict>
