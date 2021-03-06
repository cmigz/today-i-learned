# Today I Learned How to View Git Log in Reverse (plus more)

So it turns out that if you want to view git log in reverse, the command responsible is pretty straight-forward, in that "You 
can just guess and probably get it right" kind of way. `git log --reverse`

Simple right? 

But why even view it in reverse? My use case? I'm creating a tutorial branch for something and it would be so much better if I could see those tutorial commits in the order I should make them. You know what would be even better? If I not only saw the commits in order, but the diffs with the actual tutorial code step by step. 

Simple.

1. First you're gonna want to reverse that log with `--reverse`.
1. No sense in looking at more commits than you need though, so before that, count how many commits behind head you want to view, in my case it was 10 commits behind HEAD. `git log -10 --reverse` now shows the last ten commits, in reverse order (chronological).
1. Now suppose I want to see the actual code I wrote in those commits as well.`git log -10 --reverse --patch`

![til-git-log-reverse1](https://cloud.githubusercontent.com/assets/16841950/26646835/2d248616-460b-11e7-84b9-2f5999e1f783.gif)

It can be a bit unwieldy (for example, in the following gif you'll see some commits that are the result of generator commands, generating large chunks of code.) but it is a nice way to navigate tutorial branches and the like.

You can even go one step further by searching within the log by typing `/` your search term, and pressing enter. Press `n` to go to next instance and `N` to go to last instance. For instance, I just searched the word commit, which let me jump from commit to commit (with some small exceptions where I used the word commit in a commit message)

![til-git-log-reverse2](https://cloud.githubusercontent.com/assets/16841950/26650733/608c1fe8-4618-11e7-8f17-62924fe09d60.gif)

## Examples of use

Consider showing examples in code blocks, with images/gifs or as a simple markdown list of steps.

