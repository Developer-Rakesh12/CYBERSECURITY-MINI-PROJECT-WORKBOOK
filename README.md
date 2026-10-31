# EWB Phishing URL Awareness Checker

## Overview
Phishing is a trick in which fake links or messages try to make people share passwords, OTPs or payment details. This Python command-line project reads URL text and highlights selected warning signs so a user can review a link carefully.

## Features
- Detects an `@` symbol in the URL
- Flags unusually long URLs (over 100 characters)
- Flags IPv4-address hostnames
- Flags many hostname segments (5 or more)
- Flags punycode-style hostnames (`xn--`)
- Flags the HTTP scheme
- Repeats checks in one session until the user types `q`, `quit` or `exit`
- Shows a **REVIEW CAREFULLY** summary when warning signs are found
- Handles malformed URL input without crashing

## Requirements
- Python 3.10 or later
- No extra packages are required

## How to Run
Open a terminal in this project folder.

**Windows**
```bash
python phishing_checker.py
```

**Mac/Linux**
```bash
python3 phishing_checker.py
```

Type a sample URL when prompted. Type `q` to quit.

## Example Output
```text
EWB Phishing URL Awareness Checker
Text checks only - this program does not open URLs.

Enter a sample URL (or type q to quit): http://192.0.2.10/account

Result:
- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.

REVIEW CAREFULLY: 2 warning sign(s) found.
Never enter passwords from unexpected links.
```

## Testing
Five sample cases are documented in [`tests/test_samples.md`](tests/test_samples.md). Run each sample on your own computer and verify the actual output before submitting.

## Screenshots
After running the program and verifying all five tests, save your own screenshots in the `screenshots/` folder using these exact names:
- `sample_run.png` — terminal showing the command, one sample URL and its result
- `test_results.png` — your completed test table or terminal evidence for all five tests

Do not submit fabricated screenshots. Make sure no private information is visible.

## Improvements
1. **Loop with quit command** — checks multiple sample URLs without restarting the program. Type `q`, `quit` or `exit` to stop.
2. **Review carefully summary** — displays the number of warning signs found, making the result easier to understand.
3. **Malformed-input handling** — catches URL parsing errors and displays a clear message instead of crashing.

## Limitations
This is an educational awareness tool. It only reads URL text. It does not visit URLs, scan for malware, query reputation services or prove that a URL is safe. **No warning signs found does NOT mean a URL is safe.** Some legitimate URLs may also trigger warnings.

## Ethical Use
- Use only the sample strings provided in the workbook or other harmless test strings.
- Do not collect credentials or send phishing messages.
- Do not scan or probe websites or networks without written authorisation.
- Never upload passwords, API keys or confidential data to GitHub.

## Author
- Name: RAKESH SINGH NEGI
- Batch / Course: AI-Powered Cybersecurity Internship 
- Organisation: EWB Courses
