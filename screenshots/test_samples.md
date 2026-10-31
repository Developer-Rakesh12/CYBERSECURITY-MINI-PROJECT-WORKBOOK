# Test Results

**Python version used:** Python 3.13
**Operating system:** Windows 11
**Date:** 31 October 2026 

The following are the expected results for the five supplied sample URLs. Actual results must be verified by running the program on your computer.

| # | Input                                     | Expected Result         | Actual Result                                                                                 | Pass/Fail |
| - | ----------------------------------------- | ----------------------- | --------------------------------------------------------------------------------------------- | --------- |
| 1 | `https://www.example.com/login`           | No listed warning signs | No listed warning signs found. This does NOT prove safety.                                    | Verify    |
| 2 | `http://192.0.2.10/account`               | IP address + HTTP       | Uses an IP address instead of a familiar domain; Uses HTTP. HTTPS alone does not prove trust. | Verify    |
| 3 | `http://example.com@sample.invalid/login` | @ symbol + HTTP         | Contains an @ symbol; inspect carefully; Uses HTTP. HTTPS alone does not prove trust.         | Verify    |
| 4 | `https://a.b.c.d.e.example.invalid/path`  | Many hostname segments  | Contains many hostname segments/subdomains.                                                   | Verify    |
| 5 | `https://xn--example.invalid/`            | Punycode-style hostname | Contains a punycode-style hostname.                                                           | Verify    |

## Notes

- The program checks URL text only and does not visit websites or send information anywhere.
- The checks are warning clues, not proof that a URL is malicious or safe.
- The loop, review summary and malformed-URL handling were added as improvements.
- Mark each test PASS only after verifying its actual output on your computer.
