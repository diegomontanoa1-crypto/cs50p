# Bug Log

Write down every error you hit and how you fixed it. Future you will thank you.

| Date | Week | Error message | What caused it | How I fixed it |
|------|------|---------------|----------------|----------------|
| 2026-11-03 | 0 | `AttributeError: 'str' object has no attribute 'lowercase'` | I guessed the method name. "lowercase" is how the docs *describe* it, not what it's called | Searched the string methods docs for `str.low` and found the real name, `.lower()` |
| 2026-11-03 | 0 | `TypeError: unbound method str.lower() needs an argument` | I typed `str.lower()` literally. In the docs, `str.` just means "any string" | Used my own variable instead: `text.lower()`. Also learned string methods return a *new* string, so I have to save it: `text = text.lower()` |
