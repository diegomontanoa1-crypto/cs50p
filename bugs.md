# Bug Log

Write down every error you hit and how you fixed it. Future you will thank you.

| Date | Week | Error message | What caused it | How I fixed it |
|------|------|---------------|----------------|----------------|
| 2026-11-03 | 0 | `AttributeError: 'str' object has no attribute 'lowercase'` | I guessed the method name. "lowercase" is how the docs *describe* it, not what it's called | Searched the string methods docs for `str.low` and found the real name, `.lower()` |
| 2026-11-03 | 0 | `TypeError: unbound method str.lower() needs an argument` | I typed `str.lower()` literally. In the docs, `str.` just means "any string" | Used my own variable instead: `text.lower()`. Also learned string methods return a *new* string, so I have to save it: `text = text.lower()` |
| 2026-11-03 | 0 | `SyntaxError: unterminated string literal` | Forgot the closing `"` in my `input("...")` prompt, so Python never found the end of the string | Added the missing `"`. The `^` arrow in the error pointed right at where the string started |
| 2026-11-03 | 0 | `SyntaxError: invalid syntax. Perhaps you forgot a comma?` | Wrote `text.replace' ''...'` with no parentheses and no comma between the two values | Compared it to the docs example `.replace('spam', 'eggs')`: values go inside `( )` and are separated by a comma |
| 2026-11-03 | 0 | check50/submit50: `Could not connect to GitHub, it seems you are offline` | Not my code. check50 gives GitHub only 10 seconds to answer, and CS50's repo was taking about 11 | Just retry the command (Up arrow + Enter) a few times until one gets through |
