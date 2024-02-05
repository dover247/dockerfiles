FROM kasmweb/kali-rolling-desktop:x86_64-1.14.0

USER root

# Set the environment to non-interactive
ENV DEBIAN_FRONTEND noninteractive

# Configure dpkg to not prompt for choices on package configurations
RUN echo 'Dpkg::Options { "--force-confdef"; "--force-confold"; }' > /etc/apt/apt.conf.d/local

# Update and upgrade the system without any prompts
RUN apt update -y
RUN apt install -y --no-install-recommends openvpn hurl iputils-ping hashcat nmap burpsuite metasploit-framework evil-winrm ftp python3-impacket freerdp2-x11 rdesktop ffuf wfuzz seclists wordlists jq

# Reset the environment to its default state
ENV DEBIAN_FRONTEND newt
COPY red-kali-2021-1-3840x2160.png /usr/share/backgrounds/kali/kali-moto-16x9.png