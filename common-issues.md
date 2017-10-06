### My website (`<yourname>.github.io>`) looks like [this](http://bit.ly/2jua99W), and nothing like my HTML/CSS.

Chances are you just need to rename your main webpage. Remember, your browser will look for an `index.html` file when displaying your website. If you don't have an `index.html`, you need one! An easy way to rename a file in the command line is using the `mv` command, which we'd conventionally use to **m**o**v**e a file or directory. In this case, all you need to do is `cd` into the directory containing your HTML, CSS, and/or JS files, and enter the following (without angle brackets):

`mv <old_file_name> <new_file_name>`

including file extension. For example,

`mv neils_awesome_webpage.html index.html`

That's it!

---

### I don't think my CSS is showing up.

Ensure

--- 

### How do I horizontally center an element?

Remember our center alignment hack:

```
.element {
  margin: 0 auto;
}
```

---

### How do I vertically center an element?

[This continues to be difficult](http://stackoverflow.com/questions/3931187/css-metaphysics-why-is-page-vertical-alignment-so-difficult), but I strongly recommend this method:
```
.element {
  position: relative;
  top: 50%; 
  transform: translateY(-50%);
}
```
