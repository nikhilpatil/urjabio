# urja-bio

To publish to `docs/` folder

    hugo -d ./docs  


If it's **the first time** you check-out a repo you need to use ```--init``` first:

    git submodule update --init --recursive

For **git 1.8.2** or above, the option `--remote` was added to support updating to latest tips of remote branches:

    git submodule update --recursive --remote

This has the added benefit of respecting any "non default" branches specified in the `.gitmodules` or `.git/config` files (if you happen to have any, default is origin/master, in which case some of the other answers here would work as well).

For **git 1.7.3** or above you can use (but the below gotchas around what update does still apply):

    git submodule update --recursive

or:

    git pull --recurse-submodules

if you want to pull your submodules to latest commits instead of the current commit the repo points to.

See [git-submodule(1)][1] for details


  [1]: https://www.kernel.org/pub/software/scm/git/docs/git-submodule.html