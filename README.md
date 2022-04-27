# `CMPSC 302` Web Development, Project

* Assigned: 27 April 2022, 1:30 PM
* Due: Various dates -- see table below

## Project-ing yourself

The course project offers the opportunity to achieve one of a few outcomes based on your interest in extending a course project to a meaningful degree or developing
a short project of your own. Any of these objectives may be completed individually or in a small group numbering no more than `2` people. While outcomes will vary
depending on the type of project chosen. Due to the wide variance of projects set to be pursued, I require a few interim "deliverables" to be able to both assess
and evaluate your plans along the way to ensure that projects are representative of both your individual skills and the basic learning objectives of the course.

### Deadlines

The following table outlines general dates for submission of various materials. The expected contents of these materials will be further defined in the 
corresponding documents linked in the third column.

|Type of deliverable |Date            |Documentation                                 |Word count (min)   |
|:-------------------|:---------------|:---------------------------------------------|:------------------|
|Project description | 29 April, 5:00p|[Project description](writing/description.md) |150                |
|Project update      | 6 May, 5:00p   |[Project update](writing/update.md)           |250                |
|Project final report| 18 May 11:59p  |[Project report](writing/report.md)           |500                |

Failure to submit any one of these pieces will cause the assignment to be considered "Ignored" under the terms of the course contract. "Ignored" assignments
mean automatic failure in the course.

### File requirements

Unless otherwise convincing me in writing (likely in the [description](writing/description.md) document, you are required to:

* deploy static page content in the `docs/` directory using GitHub Pages
* deploy nodeJS content using the `app/` directory, likely using Heroku, though there are other services out there
* share Web3 contracts using the `contract/` directory (you'll likely deploy elsewhere, but at least include it in your repository)
  * depending on your level of experience, you may need to meet with me for a short tutorial of how to do this

#### A note on Web3

Your implementation of Web3 work _should cost you nothing_ (that means, no real tokens and no cash expenditure). To do this _be sure you are deploying
to a testnet, preferably Rinkelby_.

### Other requirements

* Your `docs/` directory work should pass both the `HTML` and `CSS` validators
* Pages should continue to pass basic accessibility checks (contrast, clear labeling)
  * Based on the project you choose, these objectives might need to be adjusted

## Kickstarting your process

The project should either:

* extend a project we've achieved in class so far
* implement a new project of your own design

As written above, no more than `2` people can work together on the project, and they _must submit the same repository_. This will mean:

* using `branch`es
* `Pull Requests`

and other skills at your disposal to collaborate (if choosing the team path). Be sure you are either confident with these skills or open to a learning process
if you choose the collaborative route.

### Ideas for extending projects

If choosing to extend a project, I invite you to consider the following strategies:

1. What project represented the area of web development that most excited you, or about which you want to learn more?
2. Develop at least `5` ideas to choose from in extending the project.
  * Meaningful project extensions include some concept or approach about which you're currently somewhat "foggy" (i.e. not 100% certain of)
3. Copy the `docs/` and any other relevant folders _over_ those included in this repository

### Ideas for developing projects

For those choosing to develop a project from scratch:

1. What specific area or set of technologies would you like to explore most?
2. Develop a short statement (no more than 1-2 sentences) defining the outcome for at least `3` potential projects.
3. Consider the skills in which you feel you're strongest; how can you develop something potentially "portfolio-worthy"?

## Making a GitHub Pages page

This assignment also requires you to make your work available via GitHub Pages. For a primer on where to find it
and how to do it:

- [ ] locate and click the `Settings` tab at the top of the screen
- [ ] from the menu at the left, select `Pages`
- [ ] locate the "Source" heading; set the "Branch" as `main`, and change the second drop-down to `/docs`
- [ ] click `Save`
- [ ] One last step: make the page _public_ by setting `GitHub Pages visibility` to `Public`
  * This step is _required_ for your HTML and CSS to pass validation!

A green box will appear at the top of the page listing the random URL that you've been assigned. This is your
URL!

## Setting up a Heroku app

### Creating an app

To do the server ("back-end") part of this assignment, you'll need to head over to [Heroku](https://www.heroku.com) and create
a free account. Once you've created one:

1. Log in and find the `New` button (it's in the upper left corner)
2. Click `Create new app` and name it: `cmpsc-302-chat-server-YOUR_GITHUB_USERNAME`
3. Click `Create app`
4. On the resulting screen, locate the `Deployment` section
5. Click `GitHub`
6. Connect Heroku to your GitHub account
7. Once you've linked the account, select the `Allegheny-ComputerScience-302-S2022` organization
8. Search for your repository and link it
9. As a final step, set up automatic deploy from the `main` branch

Once you've linked the repository, any `push` you make to your GitHub repository will also build the `app` directory on Heroku
at the address:

```
APP_NAME.herokuapp.com/
```

### Setting up "Buildpacks"

To tell the Heroku app exactly what it is (i.e. that it's a Node app) and that we need to build our app from the `app/` folder
(rather than `docs/` -- the "client" side).

The order of operations matters here, so follow steps closely!

1. Locate the `Settings` menu option near the top of the screen
2. Scroll to the `Buildpacks` section
4. Click `Add buildpack``
3. Add the `https://github.com/timanovsky/subdir-heroku-buildpack.git` repository to the app
4. Also search for and add the `heroku/nodejs` pack

## Accepting the assignment

- [ ] Using either the link posted to our class Discord or the [course schedule](https://cmpsc302.chompe.rs)
- [ ] Click the link provided for the lab assignment and accept it in GitHub classroom
- [ ] Once the assignment finishes building, click the link to go to your personal repository assignment

## "Cloning" a repository

### Using the correct download link

- [ ] On this repository's page, click the `Clone or download` button in the upper right hand corner
* You may need to scroll up to see it
- [ ] In the upper right corner of the box that appears, click `Use SSH`
- [ ] Copy the link that appears in the textbox below the phrase "Use a password with a protected key."

#### Cloning

* [ ] Type `ls` in your terminal window
* You should be in your `~` directory
- [ ] Find the folder you've made to hold class assignments (may involve `cd`ing)
- [ ] Once there, "clone" the repository using the link copied above
  * If I (the instructor) were to clone my own repository, I'd enter (your link will look different):

```
git clone git@github.com:Allegheny-ComputerScience-302-S2022/cmpsc-302-project.git
```

## Wrap-up

### Submitting the assignment/saving progress

The GitHub platform is a place to store your work. So, it makes some sense that should be able to _clone_ (download) from it, and push back (upload) to it. Here, we'll learn this second part.

- [ ] `cd` to your `~` folder
- [ ] Locate your `cmpsc-302-project` folder and `cd` to it.

Once in this folder, we need to tell git that there have been changes.

- [ ] Type `git add -A` and press `Enter`
* This tells git to look through the _entire_ folder structure for new changes and "stage" them

- [ ] Type `git commit -m "YOUR COMMIT MESSAGE"` to "label" the commit
* This is typically something like `git commit -m "Fixing a typo"` -- the message in quotes should be as descriptive as possible, while still remaining somewhat short

- [ ] To send all changes to the server, type `git push`
- [ ] At the prompt, input the password associated with the `SSH Key` you created earlier in this exercise (yesterday)

Once the process finishes successfully, we're done!
