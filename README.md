# CVE-2024-54772 (MikroTik-RouterOS Username Enum)
This repo contains the exploit for **CVE-2024-54772** which can enumerate valid usernames (using a wordlist) in Mikrotik routers running RouterOS **stable** versions **v6.43** through **v7.17.2**. The patch is available in **v6.49.18** and  **v7.18**. For **long-term** release, affected versions are **v6.43.13** through **v6.49.13**. Please, check the following link for [RouterOS change log](https://mikrotik.com/download/changelogs)

**"mikrotik_routeros_username_enum.py"** Usage: `python3 mikrotik_routeros_username_enum.py <username> <target>`. The output will be either a valid or invalid username.

**"mikrotik_routeros_username_enum_wordlist.py"** Usage: `python3 mikrotik_routeros_userenum_wordlist.py <wordlist_path> <target1,target2,...>`. The output will be all the valid usernames for every router ip entered.

Please, note that every username is sent in a seperate tcp session because RouterOS doesn't respond to the requests sent after 3 tries in the same tcp session.

I created 3 Nmap modules concerning MikroTik-RouterOS. Pleace, check them here(https://github.com/nmap/nmap/pull/2973)

Please, Read the following report: [vulnerability_poc.pdf](https://github.com/user-attachments/files/18760078/vulnerability_poc.pdf)

**Reference:** https://www.cve.org/CVERecord?id=CVE-2024-54772

