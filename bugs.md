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
| 2026-11-03 | 0 | (no error, would have frozen) `300000000 ** 300000000` | Used `**` with the big number twice. That's "to the power of 300 million", not squared | Squared means `** 2`. Also: the function should square its parameter, not a hard-coded number |
| 2026-11-03 | 0 | `TypeError: unsupported operand type(s) for *: 'int' and 'function'` | Wrote `m * square`, which multiplies by the function itself instead of calling it | Call it with `( )` and a value: `square(300000000)` |
| 2026-11-03 | 0 | `return square` / `return squared` (wrong name) | Returned the function's name, or a variable that didn't exist | Return the variable that actually holds the result |
| 2026-11-03 | 0 | (idea) `.remove()` on a string | `.remove()` is a list method. Strings don't have it | Used `.replace('$', '')`. Replacing with an empty string removes it |
| 2026-11-03 | 0 | `float(input)` | `input` is the name of Python's function, not what the user typed | Pass the variable holding the text: `float(new_number)` |
| 2026-11-03 | 0 | `ValueError: could not convert string to float: '$50.00'` (would happen) | Did `.replace()` into `newNumber` but then converted `d`, which still had the `$` | `.replace()` never changes the original. Convert the variable that holds the cleaned text |
| 2026-11-03 | 0 | Returned text instead of a number | Converted into `d` but returned `newNumber`, which was still a string | Keep track of which variable has the latest version, and return that one |
| 2026-11-03 | 0 | Named a variable `dollars_to_float` inside `dollars_to_float` | Reused the function's own name for a variable. It works, but it's confusing | Pick a different, descriptive name, like `amount` |
| 2026-11-03 | 0 | `15 // 100` gave `0` | `//` is floor division, which throws away the decimals | Use `/` for normal division: `15 / 100` gives `0.15` |
| 2026-11-03 | 0 | Got `Leave $750.00` instead of `$7.50` | `p / 100` on its own line calculated `0.15` and threw it away, so `p` stayed `15.0` | A result is only saved if `variable =` is on the same line: `p = p / 100` |
| 2026-11-03 | 0 | `>>> python tip.py`: `SyntaxError: invalid syntax` | I was still inside the Python prompt (`>>>`), which only accepts Python code | Type `exit()` to get back to `$`, then run programs from there |
| 2026-11-03 | 0 | `python: can't open file '.../tip.py': No such file or directory` | Ran it from my main folder instead of the `tip` folder | `cd tip` first. The prompt shows which folder I'm in |
| 2026-11-03 | 0 | `cd indoor`: `No such file or directory` | I was already inside `indoor/`, and there's no `indoor` inside `indoor` | Check the prompt before using `cd` |
| 2026-11-03 | 0 | submit.cs50.io showed "No results" for Faces | The upload worked, but CS50's automatic check never finished | Resubmitted. Only results with a score (like 4/4) count on cs50.me |
| 2026-11-03 | 0 | `git clone`: "You are in a repository managed by CS50. Git is disabled." | My default folder is already a git repository run by CS50, so git is turned off there | `cd /workspaces` first, then clone. My notes repo lives at `/workspaces/cs50p` |
| 2026-11-03 | 0 | cs50.dev stuck on "Building codespace" / `deadline exceeded` | Too many codespace tabs open, plus a stuck `/restart` tab | Close all codespace tabs, restart Chrome, and open cs50.dev in **one** tab only |
| 2026-11-03 | 0 | check50 on Windows: `No module named 'termios'` | CS50's tools only run on Linux/Mac | Use cs50.dev, where the tools come preinstalled |
