# Norwegian WiFi Wordlist 🇳🇴

A 20 million entry wordlist optimized for Norwegian WiFi networks, designed for authorized penetration testing and security research.

## Features

- **20M passwords** prioritized from most to least likely
- **Norwegian-specific patterns**: names, places, football teams, cultural words
- **ISP default patterns**: Netgear (adjective+noun+3digits), Telenor, Altibox styles
- **Keyboard walks**: Norwegian keyboard layout patterns

## Quick Start
```bash
# Download the wordlist
wget https://github.com/Gabrielkvaal/Norwegian-WiFi-Wordlist/releases/download/v1.0/norwegian_wifi_20M.zip
unzip norwegian_wifi_20M.zip

# Use with wifite
wifite --dict norwegian_wifi_20M.txt

# Use with hashcat
hashcat -m 22000 -a 0 capture.hc22000 norwegian_wifi_20M.txt
```

## Priority Structure

1. **Top weak passwords** - qwerty123 (#1 in Norway), 123456, password
2. **Keyboard walks** - Norwegian layout patterns (æøå)
3. **Name + year** - Ole2024, Lars1990, Kari2023
4. **Place names** - Oslo123, Bergen2024, Trondheim
5. **Football teams** - Rosenborg, Valerenga, Brann + numbers
6. **Norwegian words** - fjord, hytte, sommer + variants
7. **Compound words** - sommerhytte, vintertur, fjelltur
8. **L33t speak** - h3mm3lig, pa55ord
9. **Netgear patterns** - quietunicorn604, reddragon123
10. **ISP-style** - Word+Number+Word patterns

## Research Sources

- NordPass Norwegian password statistics (qwerty123 is #1 in Norway)
- Netgear default password patterns (adjective+noun+3digits)
- Norwegian ISP router configurations
- Norwegian cultural data (SSB name statistics)

## Legal Disclaimer

⚠️ **For authorized security testing only.** 

Only use this wordlist on networks you own or have explicit written permission to test. Unauthorized access to computer networks is illegal.

## License

MIT License - Use responsibly.