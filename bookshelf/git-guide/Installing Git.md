# Installing Git

You don't install git yourself. Your agent does it, and it never holds anything up: setup builds your house without git, starts git's install if your computer doesn't have it yet, and carries on. When git arrives, your agent turns on version history in both folders of your house by itself. This page says what happens, and what your part is.

## What your agent does

1. **It checks.** It asks your computer whether git is there (`git --version`, and on a Mac `xcode-select -p`).
2. **If git is missing, it starts the install** and carries on with whatever you were doing.
3. **It writes itself a note** in its memory: "git: installing."
4. **Each session, it checks again.** When git has arrived, it sets up version history in your agent home and your HQ (`git init`, the kit's `.gitignore`, a first commit in each), updates its note, and tells you in one sentence.

If git was already on your computer, steps 2 and 3 never happen.

## Your part, on a Mac

On a Mac, git comes with Apple's developer tools. Your agent starts their install (`xcode-select --install`), and Apple shows a dialog asking whether to install them.

- Click **Install**, then **Agree** to the license.
- The dialog sometimes appears *behind* other windows. If nothing seems to happen, look behind your open windows, or use Cmd+Tab to look for an "Install" window.
- The time estimate is wildly inaccurate at first — it may say 16 hours. It usually takes minutes; on a slow connection it can take an hour or more. The progress bar may restart partway through. That's normal.
- You can keep working with your agent the whole time.

If the dialog says the tools are already installed, git is already there; tell your agent.

<!-- VERIFY(cold-start): whether xcode-select --install can be started from a Code-tab session -->

## Your part, on Windows

On Windows, your agent installs Git for Windows with Windows' own package manager (`winget install --id Git.Git -e`). Windows may ask you to allow the install; read the prompt, and say yes if it's Git for Windows.

Git for Windows brings Git Bash with it. You won't use it yourself, but your house's hooks run under it, so leave it installed.

<!-- VERIFY(cold-start): whether winget is present on a fresh Windows 11, and whether its install asks for approval -->

## If something goes wrong

- **The Mac dialog disappeared before it finished.** Ask your agent to start it again.
- **Your agent says git still isn't there after a long while.** Ask it to check your setup (the `check-my-setup` skill, if your house has it, or just "is git installed yet?"). It will tell you the smallest next step.
- **Git asks "who are you" at the first commit.** Git needs a name and an email for your history. Your agent asks you for the name you'd like on it and an email you use, and sets them.

## Next

[Your GitHub Account](Your%20GitHub%20Account.md) — optional: an account on GitHub, if you ever want a copy of your work off your computer or to collaborate. A house doesn't need one.
