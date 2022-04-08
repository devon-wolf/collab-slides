---
theme: default
class: 'text-center'
highlighter: shiki
lineNumbers: true
info: |
  ## Gitting Along Slides
drawings:
  persist: false
---
# Gitting Along

Talking to Humans and Coding Collaboratively

<!-- notes -->

---
layout: center
---

# Agenda

- Collaborating in the Wild
- Communication and Process
- Feature Branching with Git
- Stopping Merge Conflicts before They Start

<!-- notes -->

---

# About Me

Devon Wolfkiel
- Consulting Engineer at CDW
- Alchemy grad, June 2021
- Alchemy TA, April 2021 cohort
- Ex- knifemaker, house painter, and book editor

<!-- notes -->

---

# This Talk is Not About

- Using git flawlessly
- The specific preferences or workflow of any given team
- Anything especially technical

<!-- notes -->

---

# This Talk is About

- Making team agreements
- Preventing conflicts
- Writing nice, readable PRs

<!-- notes -->

---

# Why?

As you start your careers as developers, it can take a while for your peers to see your chops.
- Pull requests may be the main way your team members get to know your work.
- A thoughtful, focused pull request shows you see the big picture, that you know how to work in a team, and that you are doing your part to make a complicated job easy.
- On the other hand, a messy, overreaching pull request slows down the team, can introduce hard-to-parse conflicts, and adds a new layer of work when you have to fix it.

<!-- notes -->

---
layout: center
---

# Collaborating in the Wild

<!-- notes -->

---

# You Will Work with Other People
and it will probably involve git
- The way work is executed on any given team is going to vary, but in general, part of what you do most days as a programmer will involve combining something you're working on right now with something someone else has worked on or is going to work on.
- "You, in the past" and "you, in the future" are also other people!
- This can get messy, even with the best laid plans. When things get messy, people need to move more slowly to navigate through the mess.

---

# CONTRIBUTING.md

- Ideally, projects you work on will have some documentation about setup, preferred conventions, etc. This tends to live either in the README or a doc called CONTRIBUTING or something similar.
- If they don't: **ask**, and record the answers! If it's a solo project or one where you're the main dev: **write it**!
  - Seriously - "you, in the future" will thank you when they forget how to spin up that weird-but-cool abandoned repo lurking on your hard drive.

<!--
  switch over to a sample project and write up a CONTRIBUTING doc, continue with the doc as we continue through the slides
 -->
---
layout: center
---

# Communication and Process

<!-- 
- team should agree on the processes to be used on the project
- the process should be *documented* for ease of reference and onboarding of new team members; this helps provide accountability and is also just easier
- in this section, let's create a CONTRIBUTING.md that lays out how our imaginary team is going to agree to work together
-->

---

# Talk to People
- if you don't know how your team likes to handle collaboration, **ask**
  - if it's not written down anywhere, **write it down**, ideally where new devs on the project can find it

---
# Tests

- A codebase without tests is broken code - either waiting to happen, or that has already happened and you just haven't noticed.
- If your team doesn't have standards in place for what to test, **put them in place**.
- If you add a new feature, add a test for that feature. If you fix a bug, make sure there's a test to show it's fixed.
- Tests are not just for testing - they're also documentation and make reviewing code much easier.

---
layout: center
---

# Feature Branching with Git

<!-- notes -->

---

# Git is Expansive
- there is so, so much you can do with git and the collaboration tools that have built up around it - try not to worry about this
- being thoughtful about your changes and making sure you keep your code up to date is way, way more important than being able to effortlessly rebase or cherry-pick commits

---

# A Common Workflow
- start on `the-branch-we-merge-all-the-stuff-to` and run `git pull origin the-branch-we-merge-all-the-stuff-to` to make sure it's up to date, then:

<br />

- `git checkout -b feature/some-new-feature`
  - *write some very groundbreaking and amazing code, run any formatting steps*
- `git add -A`
- `git commit -m 'adds my super cool changes'`
- `git pull origin the-branch-we-merge-all-the-stuff-to`
  - *if there are conflicts, resolve them and commit the changes*

<br />
probably run through the above steps a few more times, or maybe go straight to:

- `git push origin feature/some-new-feature`
---

# Now We Make a Pull Request

- I find it useful to review my changes and write up a short list of the meaningful things this new code is meant to accomplish

---
layout: center
---

# Stopping Merge Conflicts before They Start

<!-- notes -->

---

# Why Do Merge Conflicts Happen?

- Merge conflicts are going to happen - when more than one person makes changes to the same section of code, there will need to be some manual intervention to tell git which changes should be kept. This is normal and good.
- Our goal, then, is to catch these conflicts early so we can reason about them more clearly, and to try to minimize unnecessary conflicts.

<!-- notes -->

---

# How to Minimize Merge Conflicts
<br />
<br />

## Pull down often
The more you pull in fresh code, the smaller and less cumbersome any merge conflicts will be.

## Focus on the task at hand
The more your scope grows, the more conflicts you may introduce, and the harder it is to think about them.

---

# More Minimizing Merge Conflicts
<br />
<br />

## If you change something big, push early
- Big changes are more likely to touch everyone's code, so you'll want your team to have the latest version ASAP.
- If they came as a surprise while you were working on something else, consider whether you should make these significant changes as part of their own branch.

## Have a plan
Knowing what you intend to be working on before you start will help will all of the above.

---

# Summary

- Communicate about what you and the people you're working with expect.
- Make sure you are working with the freshest code.
- Keep your branches focused.
- Write tests.

---
# Resources and Links
### Git guides:
- [Git intro, overview, and commonly used commands](https://rubygarage.org/blog/most-basic-git-commands-with-examples) from RubyGarage
- [Gitflow workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) and [trunk-based development](https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development) from Atlassian
- GitHub's [pull request documentation](https://docs.github.com/en/pull-requests)

<br />
<br />

### Other:
- [docs](https://docs.npmjs.com/cli/v8/commands/npm-ci) for the `npm ci` command, which removes existing node modules, looks at an existing `package-lock.json`, and installs dependencies based on the `package-lock` - this can be especially useful if/when your `package-lock` gets out of sync with your team

<br />
<br />

---

# More Resources

### Discussions and food for thought:
- [HackerNews thread](https://news.ycombinator.com/item?id=30712175) about people's preferred git commit/push patterns
- [Tips for code reviews](https://betterprogramming.pub/5-rules-for-every-code-review-98bf60dd5dbe) by Israel Miles on Medium

<br />
<br />

### Where to find me:
- [GitHub](https://github.com/devon-wolf)
- [LinkedIn](https://www.linkedin.com/in/devon-wolfkiel)
- [My resume](https://devon-wolf.github.io/resume/), if you want it?