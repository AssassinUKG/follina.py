# 'Follina' Microsoft Office RCE

Quick POC to replicate the 'Follina' Office RCE vulnerability for local testing purposes. Running the script will generate the `clickme.docx` payload file in your current working directory, and start a web server with the payload file (`www/exploit.html`). The web server listens on all interfaces by default, but the payload file will point towards your local host for retrieving it. Modify parameters in `follina.py` as needed.

As far as I'm aware the file that is executed needs to end in `.exe`, but you can load it from a remote file share to farm some hashes if you want. Alternatively, you can adapt the payload to run encoded powershell as observed in the original payloads, described by Kevin Beaumont in the blog linked below.

Usage: `python3 ./follina.py`

> ⚠ DO NOT USE IN PRODUCTION LEST YOU BE REGARDED A DUMMY

Thanks to [Kevin Beaumont](https://twitter.com/GossiTheDog) for [his original analysis](https://doublepulsar.com/follina-a-microsoft-office-code-execution-vulnerability-1a47fce5629e) of the issue, [@KevTheHermit](https://twitter.com/KevTheHermit) for sharing their poc, and [John Hammond](https://twitter.com/_JohnHammond) for their further work on analysing payload requirements. Additional thanks to [@mkolsek](https://twitter.com/mkolsek) for the template [supporting Office 2019](https://twitter.com/mkolsek/status/1531217733546823681), and [@theluemmel](https://twitter.com/theluemmel) for sharing their version of the payload with me.