# fork-cleanup

Remove your unneccessary forks from github

A [blogpost on medium.com](https://medium.com/@icanhazedit/clean-up-unused-github-rpositories-c2549294ee45) gave me the idea to do this in a more safe and easier way.

Requires python 3

# How to run it

- pip3 install --user PyGithub
- git clone https://github.com/bebehei/fork-cleanup && cd fork-cleanup
- cp credentials.txt.template credentials.txt
- $EDITOR credentials.txt
  - You have to fill **either**:
    - `AUTH_TOKEN`
    - `AUTH_USER` and `AUTH_PASS`
  - [If you want to generate a token, you have to create in you profile settings a new one.](https://github.com/settings/tokens) This token has to have the `delete_repo` scope.
- ./cleanup
  - If you're not sure about this, you can also use the `--dry` option.
  - The `-v` option is also useful.

# Two Factor Auth

If you use two factor auth, you have to use a token. Any other possibility won't work.
