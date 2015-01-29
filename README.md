> This repository contains the [jekyll](jekyllrb.com/) site which is hosted on [GitHub Pages](https://pages.github.com/) at [`http://dgmde15.github.io`](http://dgmde15.github.io).

---

# DGMD E-15 (Course Site)

> People need not only to obtain things, they need above all the freedom to make things among which they can live, to give shape to them according to their own tastes, and to put them to use in caring for and about others. Prisoners in rich countries often have access to more things and services than members of their families, but they have no say in how things are to be made and cannot decide what to do with them. Their punishment consists in being deprived of what I shall call "conviviality." They are degraded to the status of mere consumers.
> [Ivan Illich](http://www.davidtinapple.com/illich/1970_deschooling.html)

In recent years, the tools and materials needed to create interactive digital and physical projects have become vastly more accessible through the rise of hardware like the Arduino, JavaScript as a first-class citizen in the world of software development, and the exploding community of libraries and tools to support people beginning to learn these skills. We think that

Our program will be structured around the creation of four gifts. Throughout the program, we will consistently return to the empathy at the core of good design. To us, gifts are among the most charming realizations of that impulse. For each project, we'll focus on the driving questions of "For whom am I making this, and why?" (and its corollary, "What defines quality?") for each genre.

The first gift will be an interactive story (developed over weeks 1–4); the next will be a computational art piece (developed during weeks 5–8); the third be a game (developed over weeks 9–12); and the final gift is one of your own conception and creation. Each of these represents a deeply human activity: we have been telling stories and playing games and making art and giving gifts since time immemorial.

Every project will have digital and physical components and suggested extensions. You're encouraged to use each sample project as a jumping-off point, but should not feel constrained by what's provided.

---

## Contributing to this site

For one of our first activities, you'll be adding yourself to [our `/people` page](http://dgmde15.github.io/people).  To do this, you have to do a lot of crap to get your local, development environment set up.

Roughly, you need to make sure that you have `git` and [`jekyll`](jekyllrb.com/) working on your local machine (which cascades to a bunch of other stuff, too).

To do this on a Mac, you'll roughly need to follow the steps enumerated [here](https://gist.github.com/aresnick/ec3e2f68b9ab8b2614a1) in your terminal.  On a Windows machine [hopefully] the process is mostly the same; however, you'll instead install [`msysgit`](https://msysgit.github.io/) first and use that as your `git` _and_ terminal installation.  This means you should be able to skip lines [one](https://gist.github.com/aresnick/ec3e2f68b9ab8b2614a1#file-setup_course_site-sh-L1) and [seven](https://gist.github.com/aresnick/ec3e2f68b9ab8b2614a1#file-setup_course_site-sh-L7) of the Mac setup, and you may need to use a different syntax to specify your home directory on [line eighteen](https://gist.github.com/aresnick/ec3e2f68b9ab8b2614a1#file-setup_course_site-sh-L18).

### Uploading media to S3

We're hosting our site on GitHub Pages, which means it's stored in a git repository.  Git is made for keeping track of text files, and [for boring reasons](https://robinwinslow.co.uk/2013/06/11/dont-ever-commit-binary-files-to-git/) it's not great to store binary (_i.e._ non-text) files in your repository.  Beyond that, GitHub Pages isn't configured to quickly serve media, so any binary files you _do_ store will be served slowly.

Instead, we're going to rely on a separate web server to do that for us.  If your photo is public on Facebook or you have it on your website or you can use the one from your Twitter profile, great!  You're done.

But if instead, you'd like to upload a photo of your own somewhere, we're going to use Amazon's Simple Storage Service (S3) to do so.  It's basically a hard drive in the sky.  You can read more about it (including tutorials and a video) [on the Tools & Materials page](http://dgmde15.github.io/tools-and-materials)

Once you've uploaded your photo to S3 (and done the boring configuration to make it publicly accessible), you should be able to embed it as your headshot.