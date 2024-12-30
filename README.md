# FUD-Tor-reverse-shell-PoC

Here is a Proof of Concept (POC) for my red team implant project, designed to be deployed using a Rubber Ducky or any other quick and opportunistic deployment method.

This is a Portable Executable (PE) for Windows that establishes a reverse shell via the Tor network while remaining persistent until the target PC shuts down. This means that the payload remains functional even in the event of a loss of connection to the host.

All dependencies are packed within the executable, including legitimate and properly signed dependencies and programs. Thus, this reverse shell does not require any third-party installation (even for Tor).

I chose to use the Tor network for the following reasons :

- Anonymity : Ensuring control over the entry node while maintaining anonymity.
- Evasion : Better evasion of firewalls by leveraging TCP traffic on port 443.
- Simplicity : Avoiding port forwarding or additional configurations. It is truly a functional plug-and-play solution.


However, I was unable to test it on an EDR, and I have concerns about its ability to bypass them due to its high entropy (7.3), which could attract attention ...



![Main](https://github.com/raphaelthief/FUD-Tor-reverse-shell-PoC/blob/main/Listening.JPG "Main")



## Installing Dependencies on the Attacker's Side :

![Install](https://github.com/raphaelthief/FUD-Tor-reverse-shell-PoC/blob/main/install_Tor.JPG "Install")



## Setup Tor network :

![Setup](https://github.com/raphaelthief/FUD-Tor-reverse-shell-PoC/blob/main/setup_hidden_service.JPG "Setup")



## Show aviable Tor network :

![Show](https://github.com/raphaelthief/FUD-Tor-reverse-shell-PoC/blob/main/Show_aviable_hosts.JPG "Show")



## Scanning the Attack Payload (using Kleenscan to avoid signature redistribution) :

![Kleenscan](https://github.com/raphaelthief/FUD-Tor-reverse-shell-PoC/blob/main/tor_reverse.JPG "Kleenscan")



## Analyzing the Payload with Windows Defender :

![Defender](https://github.com/raphaelthief/FUD-Tor-reverse-shell-PoC/blob/main/Defender_scan.JPG "Defender")



## Creating the Executable Directly from the Tool :

![make](https://github.com/raphaelthief/FUD-Tor-reverse-shell-PoC/blob/main/exe_made.JPG "make")



## Analyzing the Payload with Windows Defender :

![Defender](https://github.com/raphaelthief/FUD-Tor-reverse-shell-PoC/blob/main/Defender_scan.JPG "Defender")



## Launching the Payload on the Target PC with Defender Running :

![Running](https://github.com/raphaelthief/FUD-Tor-reverse-shell-PoC/blob/main/Demo.JPG "Running")



