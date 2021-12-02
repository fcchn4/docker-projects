FROM kalilinux/kali-rolling:latest

CMD echo "This is FCCH container for Pentesting with Kali Linux"
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -qq && apt-get upgrade -y -qq \
    && apt-get install -y whois mlocate bash-completion curl wget vim testssl.sh \
    joomscan wpscan fierce exploitdb exiv2 git dmitry dirb dirbuster \
    metasploit-framework masscan fping nikto nmap sqlmap axel ethtool \
    udptunnel enum4linux dnsrecon dnsenum dnschef cryptcat powersploit \
    ncrack magicrescue lbd hping3 hashid hash-identifier creddump7 yersinia \
    sleuthkit skipfish spike recon-ng rebind proxychains ptunnel \
    sslsplit snmpcheck smbmap set hydra webshells weevely wfuzz whatweb \
    upx-ucl windows-binaries winexe wordlists statsprocessor dos2unix expect \
    hashdeep hotpatch wafw00f voiphopper theharvester netmask netsniff-ng ngrep \
    pwnat stunnel4 swaks tcpick tcpreplay tcpdump unix-privesc-check amass \
    arp-scan arping binwalk bulk-extractor cewl commix crunch sslyze \
    theharvester dnsrecon netcat-traditional \
    && apt-get autoremove -y && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*