# Test Results

Python version used: Python 3.13 | Operating system: Windows/Linux/macOS (update to your system) | Date: Update with test date

The actual-result entries below are the expected program messages for the supplied sample inputs. Run each input on your own computer and confirm them before submission.

| # | Input | Expected result | Actual result (verify on your computer) | Pass/Fail |
|---|---|---|---|---|
| 1 | https://www.example.com/login | No listed warning signs | No listed warning signs found. This does NOT prove safety. | PASS |
| 2 | http://192.0.2.10/account | IP address + HTTP | Uses an IP address instead of a familiar domain; Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 3 | http://example.com@sample.invalid/login | @ symbol + HTTP | Contains an @ symbol; inspect carefully; Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 4 | https://a.b.c.d.e.example.invalid/path | Many hostname segments | Contains many hostname segments/subdomains. | PASS |
| 5 | https://xn--example.invalid/ | Punycode-style hostname | Contains a punycode-style hostname. | PASS |

## Notes
- The program checks URL text only and does not visit websites or send information anywhere.
- The checks are warning clues, not proof that a URL is malicious or safe.
- The loop, review summary and malformed-URL handling were added as improvements.
