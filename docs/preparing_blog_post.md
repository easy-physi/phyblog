---
id: prepare_post
title: Preparing a Blog Post
---


### Step 1: Fork repo
If you are someone who wants to contribute an article to this blog then first
start by forking this repo by clicking on the Fork button.
![Fork](/img/preparing_blog_post/fork.PNG)

### Step 2: Create branch
Create a new branch from branch master in the forked repo.
![Branch](/img/preparing_blog_post/branch.png)

### Step 3: Create draft
In the [drafts folder](https://github.com/easy-physi/phyblog/tree/master/website/static/drafts/)
create a new markdown file. Copy and paste the following text right at the top
of the newly made file:
```
---
title: Blog Title
author: Author Name
authorURL: URL to reach author at
---
```
Explanation of the fields and other options:
 * `author` - The text label of the author byline.
 * `authorURL` - The URL associated with the author. This could be a Twitter, GitHub, Facebook account, etc.
 * `authorFBID` - The Facebook profile ID that is used to fetch the profile picture.
 * `authorImageURL` - The URL to the author's image. (Note: If you use both `authorFBID` and `authorImageURL`, `authorFBID` will take precedence. Don't include `authorFBID` if you want `authorImageURL` to appear.)
 * `title` - The blog post title.

The file created will not be considered a valid blog post file without the above
meta data at the top of the file.

Use the `<!--truncate-->` marker in your blog post to represent what will be shown as the summary when viewing all published blog posts. Anything above `<!--truncate-->` will be part of the summary. For example:

```markdown
---
title: Truncation Example
---
All this will be part of the blog post summary.

Even this.

<!--truncate-->

But anything from here on down will not be.

Not this.

Or this.
```
If you are new to formatting text with markdown it is strongly recommended that
you read our [markdown wiki](https://github.com/easy-physi/phyblog/wiki/Getting-started-with-Markdown)
first before continuing.

### Step 4: Add static assests
You can even add images to your post. Create a folder under `website/static/img/`
with the same name as that of the draft file. Dump all your images into this
folder. Once the images have been put in the correct folder you can then use them
in your blog post file as
```
![alt text](../img/<folder_name>/<image_name_with_extension>)
```

### Step 5: Create pull request
Once you are satisfied with your work you can submit a pull request (PR) to the
master branch of this repo.

### Step 6: Receive feedback
Once you submit a pull request the community can comment under your PR and give
you valuable feed back. Please read our [community code](https://github.com/easy-physi/phyblog/blog/master/CODE_OF_CONDUCT.md).
Use the available feedback to fix the issues or update citations as necessary.

### Step 7: Put up a green flag
When you, as part of the community, are confident about the work use the `publish`
label on your PR. If everything seems right then your post will soon be published
on this blog. Hooray!