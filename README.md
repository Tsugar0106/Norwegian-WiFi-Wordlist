# Norwegian WiFi Wordlist 🇳🇴

A 20 million entry wordlist optimized for Norwegian WiFi networks, designed for authorized penetration testing and security research.

## Download

**Full wordlist (20M passwords):** [Download from Releases](https://github.com/Gabrielkvaal/Norwegian-WiFi-Wordlist/releases/download/v2.0/norwegian_wifi_v2.zip)

## What's New in v2.0

- **Telenor pattern discovered**: `adjective + 3digits + noun` (Norwegian words)
- **Number priority optimization**: 5XX-6XX tested first (based on statistical analysis)
- **ASCII-safe Norwegian**: No æøå for maximum compatibility
- **20.3M passwords** with research-backed word categories

## Features

- **20M passwords** prioritized from most to least likely
- **Norwegian-specific patterns**: names, places, football teams, cultural words
- **ISP default patterns**: Telenor (adj+digits+noun), Netgear (adj+noun+digits)
- **Keyboard walks**: Norwegian keyboard layout patterns

## Quick Start

```bash
# Download to Parrot/Kali
cd /usr/share/wordlists
sudo wget https://github.com/Gabrielkvaal/Norwegian-WiFi-Wordlist/releases/download/v2.0/norwegian_wifi_v2.zip
sudo unzip norwegian_wifi_v2.zip
sudo rm norwegian_wifi_v2.zip

# Use with wifite (no WPS)
wifite --dict /usr/share/wordlists/norwegian_wifi_v2.txt --no-wps --kill

# Use with hashcat
hashcat -m 22000 -a 0 capture.hc22000 norwegian_wifi_v2.txt

# Use with aircrack-ng
aircrack-ng -w norwegian_wifi_v2.txt capture.cap
```

## ISP Default Password Patterns

### Telenor (Norwegian ISP)
```
Structure: adjective + 3digits + noun
Examples:  gra542rev, bla891fjord, stor367elg
Language:  Norwegian (ASCII-safe)
```

### Netgear (Common worldwide)
```
Structure: adjective + noun + 3digits  
Examples:  quietunicorn604, reddragon123, blueocean542
Language:  English
```

## Priority Structure

The wordlist is ordered from most to least likely:

1. **Top weak passwords** - qwerty123 (#1 in Norway), 123456, passord
2. **Keyboard walks** - Norwegian layout patterns
3. **Name + year** - Ole2024, Lars1990, Kari2023
4. **Place names** - Oslo123, Bergen2024, Trondheim
5. **Football teams** - Rosenborg, Valerenga, Brann + numbers
6. **Telenor patterns** - gra542rev, bla891fjord (~6M)
7. **Netgear patterns** - quietunicorn604, reddragon123 (~14M)

## Number Priority (Research-Based)

Based on analysis of 26 confirmed Netgear passwords:
- **5XX-6XX first** (35% of confirmed samples)
- **9XX, 4XX, 8XX next** (40% of samples)  
- **1XX last** (0% in sample - statistical anomaly)

## Sample

See `norwegian_wifi_sample_100k.txt` for the first 100,000 entries.

## Research Sources

- 26+ confirmed Netgear passwords (eBay photos, hashcat forum)
- WoNDeR-List research (Mike Allen)
- NetgearKiller wordlist analysis (fyy0r)
- NordPass Norwegian password statistics
- First-hand Telenor router observation

## Legal Disclaimer

⚠️ **For authorized security testing only.** 

Only use this wordlist on networks you own or have explicit written permission to test. Unauthorized access to computer networks is illegal.

## License

MIT License - See [LICENSE](LICENSE) for details.
