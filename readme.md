# Sítio web do CoderDojo LX

## About

CoderDojo LX's web site is hosted with Github Pages, a free service that allows users to serve static files right from a repository at a [special URL](https://coderdojolx.github.io) It uses the Hugo static webpage generator with the (updated) Cupper theme.

## Getting started

1. [Install Hugo on your machine](https://gohugo.io/getting-started/quick-start/)
2. Clone this repository into your preferred workspace by using `git clone --recursive https://github.com/CoderDojoLX/site.git`(edit if you use ssh like a cool kid)
3. `cd site` and try running `hugo server -D`and you should see an exact replica of the live site at localhost:1313

Note: if you have already cloned the repository and the project fails to build, then it's most likely because you're missing the submodules required. Run:

```
git clone --recurse-submodules --remote-submodules git@github.com:CoderDojoLX/site.git
```

## File structure

You will only need to edit the files in the `content` folder. Please avoid touching other files, it may result in the site breaking. Also avoid creating top-level files in the root content directory. You may edit the ones in the root directory but creating new files is not advised.

1. Create a post by running `hugo new post/<your file name>.md` in the site's root directory
2. Add the appropriate tags to suit the style of your post. You may view all current tags in use [here](https://coderdojolx.github.io/tags/). There is a reason why I have chosen not to display this in the menu bar...
3. Write your content in markdown. For a primer on markdown visit [this link](https://cupper-hugo-theme.netlify.app/cupper-typography/) and for specific features that Cupper offers, visit [this link](https://cupper-hugo-theme.netlify.app/cupper-shortcodes/). The note directive and the ticks directive are the most useful.

Root directory files are in English while post files are in Portuguese - this choice is arbitrary but things will break if we deviate.

You may link to your new post using the _relref directive_ `{{< relref "signup.md" >}}` in your markdown link reference. See the existing content for examples, or the helpful guides linked above.

## Updating

The usual sequence of adding, commiting, pulling, and pushing apply. If you get an error like the following

```
Fetching submodule public
fatal: remote error: upload-pack: not our ref 18fbf876b7a447c21ff2f8f62b8a8adebd215a58
```

try:

```
git submodule update --remote --merge
```

## Deploying

Deploying to the main web site is done via a script provided by Hugo and slightly tweaked by me. Run `./deploy.sh`in your local shell environment to push all the changes to the main web site.

You might have noticed that this repository does not correspond to the one used by Github Pages for publishing. This is because the default directory used by Hugo for exporting, called `public`, has been added as a Git submodule thus allowing us to separate the ready-to-serve content from the markdown files. It is in your best interest to respect this.

After deploying the site, you must now (if you are done editing) commit your changes made to the site repo. Do this as usual: `git add .` followed by `git commit -m "hello world"`and lastly `git push origin master`.

That's it, you've generated the site and updated the site repository. Your changes should now be live at [CoderDojo LX!](https://coderdojolx.github.io)
