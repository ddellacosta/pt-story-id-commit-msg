Pivotal Tracker Story ID Git commit-msg hook
============================================

If you use Pivotal Tracker a lot like I do, and have it synced up to Github or Bitbucket, you are constantly cutting and pasting story IDs into your commit messages.

Well, I'm lazy, and I didn't like the other solutions out there, so I wrote something that assumes an environment variable and prepends that to your commit message automatically, if it exists.  This means you can just set an environment variable during the time you are working on a PT story and all your commits will get this added automatically.

## How to use

  * Drop commit-msg in your repo's .git/hooks directory
  * chmod 755 .git/hooks/commit-msg
  * Set the environment variable PT_STORY_ID.  For example:

```bash
$ export PT_STORY_ID='12345678'
```

You are done.

If you don't have this variable set, it will complain but your commit will just process normally.

## TODO

  * Support for more than one PT Story ID.

2013 Dave Della Costa
[MIT LICENSE](https://github.com/ddellacosta/mit-license)
