HFL Git GUI Config 1.0.0
========================
[
  Encoding: UTF-8;
  Syntax: GitHub Flavored Markdown (GFM) <https://github.github.com/gfm/>;
]:#

Henrik Franciscus Leppä's (HFL) configurations for Git GUI (and a few rules for
Git in general).

[Git GUI and Gitk][git-guis] are useful tools for working with Git, because
they allow you to see the commit tree and pick which changes to stage, along
with many other things.

Unfortunate, they do not come with many tools/commands out of the box, and they
even lack "Applications" menu icons on some Linux distributions. This
repository is meant to fix that.

Tools include:
- "Checkout (assume remote: `origin`)"
- "Clean -- All"
- "Clean -- One File"
- "Commit -- Undo"
- "Fetch All Branches And All Submodules"
- "Fetch And Fast-Forward All Branches"
- "Filesystem Check -- Unreachable Objects"
- "Help with tools"
- "Log -- Unpushed"
- "Merge (No Fast-Forward)..."
- "Merge -- Abort"
- "Merge -- Continue"
- "Open Terminal"
- "Rebase (automatic)"
- "Rebase (get command for interactive)..."
- "Rebase -- Abort"
- "Rebase -- Continue"
- "Reference Log"
- "Reference Log (Reversed)"
- "Run Command In 'Commit Message' Field"
- "Stash -- Apply By Index..."
- "Stash -- Apply By Name..."
- "Stash -- Drop By Index..."
- "Stash -- Drop By Name..."
- "Stash -- List"
- "Stash -- Pop By Index..."
- "Stash -- Pop By Name..."
- "Stash -- Push Unstaged..."
- "Stash -- Push..."
- "Tag -- Delete"
- "Tag -- List With Message"
- "Write Commit Template"


[MIT License][]
---------------


[Changelog][]
-------------


Prerequisites
-------------

- Git GUI (`git-gui`)

  - [Comes built-in with most Git distributions.][git-guis]

- Shell scripts:

  - [`git-fetch-all-recur` - How to git fetch everything - Code
    Yarns][git-fetch-all-recur]

  - [`git-ffwd-update` - muhqu's Answer - Can "git pull --all" update all my local
    branches? - Stack Overflow][git-ffwd-update]

  - [`git-named-stash` - henrik-leppa - GitHub][git-named-stash]

  - (These scripts need to be installed in a directory found in `PATH`
    environment variable. They should not have file extensions in their
    filenames.)


Setup
-----

1. Edit `gitconfig.txt`:

   - Replace all instances of string:
     `~/INSERT/PATH/TO/REPO/HERE/gitconfig.txt` with your path to
     `gitconfig.txt` file.

   - Comment out or remove any rules you don't like under: `[core]`, `[color]`,
     `[init]`, and `[gui]` sections.

   - (Add your own tools, if you want.)

2. Link to `gitconfig.txt` file in `~/.gitconfig` by running the following in
   the terminal:
   ```sh
   git config --file ~/.gitconfig include.path '~/INSERT/PATH/TO/REPO/HERE/gitconfig.txt'
   ```

3. Optional: Add launcher to Linux "Applications" menu:

   - **Note:** This is intended for at least Linux Mint, but may work on other
     Ubuntu-based distros as well.

   - Link `git-gui.desktop` to `~/.local/share/applications` by running the
     following in the terminal:
     ```sh
     ln -s ~/INSERT/PATH/TO/REPO/HERE/git-gui.desktop ~/.local/share/applications
     ```

     - For this to come into effect, logging out and logging back in may be
       required.


[Changelog]: ./CHANGELOG.md
[git-fetch-all-recur]: https://codeyarns.com/tech/2016-05-17-how-to-git-fetch-everything.html#gsc.tab=0
[git-ffwd-update]: https://stackoverflow.com/a/9076361
[git-guis]: https://git-scm.com/downloads/guis
[git-named-stash]: https://github.com/henrik-leppa/git-named-stash
[MIT License]: ./LICENSE.md
