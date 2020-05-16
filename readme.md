# Sítio web do CoderDojo LX

## About

CoderDojo LX's web site is hosted with Github Pages, a free service that allows users to serve static files right from a repository at a [special URL](https://coderdojolx.github.io) It uses the Hugo static webpage generator with the (updated) Cupper theme.

## Getting started

1. [Install Hugo on your machine](https://gohugo.io/getting-started/quick-start/)
2. Clone this repository into your preferred workspace by using `git clone https://github.com/CoderDojoLX/site.git`(edit if you use ssh)
3. `cd site` and try running `hugo server -D`and you should see the exact same website at localhost:1313

## File structure

You will only need to edit the files in the `content` folder. Please avoid touching other files, it may result in the site breaking. Also avoid creating top-level files in the root content directory. You may edit the ones in the root directory but creating new files is not advised.

1. Create a post by running `hugo new post/<your file name>.md` in the site's root directory
2. Add the appropriate tags to suit the style of your post. You may view all current tags in use [here](https://coderdojolx.github.io/tags/). There is a reason why I have chosen not to display this in the menu bar...
3. Write your content in markdown. For a primer on markdown visit [this link](https://cupper-hugo-theme.netlify.app/cupper-typography/) and for specific features that Cupper offers, visit [this link](https://cupper-hugo-theme.netlify.app/cupper-shortcodes/).

## Deploying

Deploying to the main web site is done via a script provided by Hugo and slightly tweaked by me. Run `./deploy.sh`in your local shell environment to push all the changes to the main web site.

You might have noticed that this repository does not correspond to the one used by Github Pages for publishing. This is because the default directory used by Hugo for exporting, called `public`, has been added as a Git submodule thus allowing us to separate the ready-to-serve content from the markdown files. It is in your best interest to respect this.

After deploying the site, you must now (if you are done editing) commit your changes made to the site repo. Do this as usual: `git add .` followed by `git commit -m "hello world"`and lastly `git push origin master`.

That's it, you've generated the site and updated the site repository. Your changes should now be live at [CoderDojo LX!](https://coderdojolx.github.io)
