## "I'm getting *xyz* error when I try to do `git push`."

If you're able to `git init`, `git remote add origin`, `git add`, and `git commit` without issue, but can't `git push` (usually due to an error about SSL certificates, if you're running Windows), fret not. Follow these steps:

1. Install an FTP client, like [FileZilla Client](https://filezilla-project.org/). This lets you copy files from your computer to our JADE server.
2. For the **IP** or **Host**, enter `45.55.191.36`. For the **Username**, enter `hacker`. For the **Password**, enter `<pw
found on GroupMe>`.
3. Select *the directory that contains* all the files on your computer that make up your personal website. At the very least, this directory should include an `index.html`. Most of you will also have a `<filename>.css`, a `<filename>.js`, and/or other `.html` files. For example:
  ```
  neils-personal-site/
    ├── index.html
    ├── styles.css
    ├── script.js
  ```
    In this case, we'll upload the `neils-personal-site` directory.

4. Open **powershell** and type `ssh <SERVER>`. If this doesn't work for you, then install an SSH client, like [PuTTY](http://www.putty.org/), and enter `<SERVER>` as the **Host**, `<USERNAME>` as the **Username**, and `<PASSWORD>` as the **Password**.
5. `cd` into your personal site directory, which should now be on the server. For example, `cd neils-personal-site`. If I `ls` the contents of `neils-personal-site`, I should see my `index.html`, `styles.css`, and `script.js`.
6. Update the git config settings, just to make sure commits get attribued to you:
  `git config user.name "Jane Doe"`
  `git config user.email "Jane.Doe@columbia.edu"`
7. Perform your normal git workflow!
  - `git pull origin master` to make sure you have all your remote files in your local repository (your laptop)
  - `git add -A` to track all files in your personal website directory
  - `git commit -m "your useful commit message here"` to record the changes you made to your code
  - `git push origin master` 
8. Wait a few minutes for GitHub to update your website, then visit `<your_username>.github.io`. Your site should be up!

## What's going on here?
Normally, `git push` sends files from your local (on your computer) repository to your remote (on GitHub's _~cloud~_) repository. This works for most people. Sometimes, though, configuration issues are too hard or involved to fix, so we're using our JADE server as a middleman. Essentially, instead of this:
```
local repo ---push---> remote repo
```
we're doing this:
```
local repo ---upload--> JADE server ---push--> remote repo
```
Why? Because we know file upload/transfer (FTP) clients like Filezilla work just fine on Windows, but `git` can sometimes have trouble. So we've moved all our `git` work to our server, which we know always runs `git` just fine. Whenever you make changes and want to `git push`, unfortunately, you'll have to reupload your files from your local repository to our JADE server. 
  
  That means you should probably test more often locally (e.g. by viewing your page through `C:/Users/youruser/Desktop/.../index.html`), then upload and push only when you need to. Remember, `git push`ing to your `username.github.io` repository will update your website at `username.github.io` for the world to see!
