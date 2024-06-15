# PPPwnUI
PPPwnUI is a program that adds an UI to the exploit [PPPwn](https://github.com/TheOfficialFloW/PPPwn/) created by [TheFlow](https://github.com/TheOfficialFloW/).

## Installation

- Clone the repository:

```sh
git clone https://github.com/B-Dem/PPPwnUI
```

- Install the requirements:

```sh
pip install -r requirements.txt
```

## Usage

- Launch the app with

  **Windows :**
  
  ```PPPwnUI.bat```

  **Linux :**

  ```sh
  chmod +x PPPwnUI.sh
  ```

  Then :
  
  ```sh
  ./PPPwnUI.sh
  ```

- Select your Interface using the drop-down menu

- Choose Between the Exploit Version you want to use ([PPPwn Python](https://github.com/TheOfficialFloW/PPPwn), [PPPwn_Go](https://github.com/BestPig/PPPwn_go) & [PPPwn_CPP](https://github.com/xfangfang/PPPwn_cpp))

- Choose your Payload Between 

- PPPwn : (Available for : 7.00, 7.01, 7.02, 7.50, 7.51, 7.55, 8.00, 8.01, 8.03, 8.50, 8.52, 9.00, 9.03, 9.04, 9.50, 9.51, 9.60, 10.00, 10.01, 10.50, 10.70, 10.71 & 11.00)

- PPPwn Goldhen Payloads (Available for : 9.00, 10.00, 10.01 & 11.00)

- VTX HEN (Available for : 9.03, 10.50 & 10.70)

- PPPwn Linux Payloads (Available for : 11.00) 

- Custom Payloads (Your own custom Payloads)
 

- Then click on **Start PPPwn** to start the Exploit


## PPPwn Usage

On your PS4:

- Go to `Settings` and then `Network`
- Select `Set Up Internet connection` and choose `Use a LAN Cable`
- Choose `Custom` setup and choose `PPPoE` for `IP Address Settings`
- Enter anything for `PPPoE User ID` and `PPPoE Pasword`
- Choose `Automatic` for `DNS Settings` and `MTU Settings`
- Choose `Do Not Use` for `Proxy Server`
- Click `Test Internet Connection` to communicate with your computer

If the exploit fails or the PS4 crashes, you can skip the internet setup and simply click on `Test Internet Connection`. If the script fail or is stuck waiting for a request/response, abort it and run it again on your computer, and then click on `Test Internet Connection` on your PS4.

### Goldhen Usage

On your Computer: 

- Copy `goldhen.bin` to the root directory of an exfat/fat32 USB and insert it into your PS4.

#### Example run

```sh
[+] PPPwn - PlayStation 4 PPPoE RCE by theflow
[+] args: interface=enp0s3 fw=1100 stage1=stage1/stage1.bin stage2=stage2/stage2.bin

[+] STAGE 0: Initialization
[*] Waiting for PADI...
[+] pppoe_softc: 0xffffabd634beba00
[+] Target MAC: xx:xx:xx:xx:xx:xx
[+] Source MAC: 07:ba:be:34:d6:ab
[+] AC cookie length: 0x4e0
[*] Sending PADO...
[*] Waiting for PADR...
[*] Sending PADS...
[*] Waiting for LCP configure request...
[*] Sending LCP configure ACK...
[*] Sending LCP configure request...
[*] Waiting for LCP configure ACK...
[*] Waiting for IPCP configure request...
[*] Sending IPCP configure NAK...
[*] Waiting for IPCP configure request...
[*] Sending IPCP configure ACK...
[*] Sending IPCP configure request...
[*] Waiting for IPCP configure ACK...
[*] Waiting for interface to be ready...
[+] Target IPv6: fe80::2d9:d1ff:febc:83e4
[+] Heap grooming...done

[+] STAGE 1: Memory corruption
[+] Pinning to CPU 0...done
[*] Sending malicious LCP configure request...
[*] Waiting for LCP configure request...
[*] Sending LCP configure ACK...
[*] Sending LCP configure request...
[*] Waiting for LCP configure ACK...
[*] Waiting for IPCP configure request...
[*] Sending IPCP configure NAK...
[*] Waiting for IPCP configure request...
[*] Sending IPCP configure ACK...
[*] Sending IPCP configure request...
[*] Waiting for IPCP configure ACK...
[+] Scanning for corrupted object...found fe80::0fdf:4141:4141:4141

[+] STAGE 2: KASLR defeat
[*] Defeating KASLR...
[+] pppoe_softc_list: 0xffffffff884de578
[+] kaslr_offset: 0x3ffc000

[+] STAGE 3: Remote code execution
[*] Sending LCP terminate request...
[*] Waiting for PADI...
[+] pppoe_softc: 0xffffabd634beba00
[+] Target MAC: xx:xx:xx:xx:xx:xx
[+] Source MAC: 97:df:ea:86:ff:ff
[+] AC cookie length: 0x511
[*] Sending PADO...
[*] Waiting for PADR...
[*] Sending PADS...
[*] Triggering code execution...
[*] Waiting for stage1 to resume...
[*] Sending PADT...
[*] Waiting for PADI...
[+] pppoe_softc: 0xffffabd634be9200
[+] Target MAC: xx:xx:xx:xx:xx:xx
[+] AC cookie length: 0x0
[*] Sending PADO...
[*] Waiting for PADR...
[*] Sending PADS...
[*] Waiting for LCP configure request...
[*] Sending LCP configure ACK...
[*] Sending LCP configure request...
[*] Waiting for LCP configure ACK...
[*] Waiting for IPCP configure request...
[*] Sending IPCP configure NAK...
[*] Waiting for IPCP configure request...
[*] Sending IPCP configure ACK...
[*] Sending IPCP configure request...
[*] Waiting for IPCP configure ACK...

[+] STAGE 4: Arbitrary payload execution
[*] Sending stage2 payload...
[+] Done!
```
##### To do : 

- Rebuild PPPwn_CPP to use Interface Name and not ID  
- Auto Updater
- PPPwn Logs in the program directly
- Code optimisation

This Program was originally made with ❤️ by [Memz](https://github.com/B-Dem) for [Sighya](https://sighya.fr).

If you find this program helpful, leave a star on the repo!

And if you got any feedback, open an issues !
