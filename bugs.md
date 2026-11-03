# Bug Log

Write down every error you hit and how you fixed it. Future you will thank you.

| Date | Week | Error message | What caused it | How I fixed it |
|------|------|---------------|----------------|----------------|
| 2026-11-03 | 0 | `AttributeError: 'str' object has no attribute 'lowercase'` | I guessed the method name. "lowercase" is how the docs *describe* it, not what it's called | Searched the string methods docs for `str.low` and found the real name, `.lower()` |
| 2026-11-03 | 0 | `TypeError: unbound method str.lower() needs an argument` | I typed `str.lower()` literally. In the docs, `str.` just means "any string" | Used my own variable instead: `text.lower()`. Also learned string methods return a *new* string, so I have to save it: `text = text.lower()` |
| 2026-11-03 | 0 | `SyntaxError: unterminated string literal` | Forgot the closing `"` in my `input("...")` prompt, so Python never found the end of the string | Added the missing `"`. The `^` arrow in the error pointed right at where the string started |
| 2026-11-03 | 0 | `SyntaxError: invalid syntax. Perhaps you forgot a comma?` | Wrote `text.replace' ''...'` with no parentheses and no comma between the two values | Compared it to the docs example `.replace('spam', 'eggs')`: values go inside `( )` and are separated by a comma |
| 2026-11-03 | 0 | check50/submit50: `Could not connect to GitHub, it seems you are offline` | Not my code. check50 gives GitHub only 10 seconds to answer, and CS50's repo was taking about 11 | Just retry the command (Up arrow + Enter) a few times until one gets through |
| 2026-11-03 | 0 | `SyntaxError: unmatched ')'` | Had one `)` too many at the end of a `.replace(...)` line | Counted the opening and closing parentheses so they match. VS Code colors each matching pair, which helps |
| 2026-11-03 | 0 | `SyntaxError: Missing parentheses in call to 'print'` | Wrote `print convert(face)`. In Python 3, `print` is a function and needs `( )` | Changed it to `print(convert(text))`. The error message even suggested the fix |
| 2026-11-03 | 0 | `SyntaxError: expected ':'` | Forgot the `:` at the end of `def convert(face)` | Every `def` line must end with `:`, like `def main():` |
| 2026-11-03 | 0 | `NameError: name 'face' is not defined` / `name 'text' is not defined` | **Scope**: each function has its own variables. `text` only exists in `main`, and `face` only exists in `convert` | `main` passes its value in with `convert(text)`, and inside `convert` I use the parameter name `face` |
| 2026-11-03 | 0 | `cd ~/playback`: `No such file or directory` | In cs50.dev, `~` means `/home/ubuntu`, not my problem set folder | Use `cd` alone to get to my problem set folder, then `cd playback` |
| 2026-11-03 | 0 | Submission uploaded but missing from submit.cs50.io | The upload worked, but the website didn't register it (GitHub was slow that day) | Ran `submit50` again. Resubmitting is safe, because CS50 uses the latest one |
| 2026-11-03 | 0 | Pasted new rows and wiped my whole `bugs.md` | Everything was still selected (Ctrl+A) when I pasted | Git keeps every pushed version, so the old text was recovered from history. Check that nothing is selected before pasting |
