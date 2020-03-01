# Awesome Software Engineering comments

A curated list of awesome Software Engineering comments.

## Good ways to capture institutional knowledge?

👍for this [comment](https://news.ycombinator.com/item?id=22455678):

> Store readme markdown files in the sourcerepo along with the code itself. Make sure during review that changes to code are reflected in the markdown.
> 
> Doesn't need to be exhaustive docs - usually just a high- to medium-level explanation of what why and how goes a long way.
> 
> Controversial/surprising/confusing choices should be documented in several places - e.g. in the readme, in a bug/ticket, in the check-in comments and also a comment in the code referencing the readme/bug/ticket for more info.

👍for this [comment](https://news.ycombinator.com/item?id=22455852):

> I’m also a big markdown-in-source advocate. However it’s major shortcoming is that it’s not accessible enough for non-technical teams to maintain.

👍for this [comment](https://news.ycombinator.com/item?id=22455535):

> Automate everything that can be automated. Avoid setting up things using GUIs.
>
> Starting a set of services should be as simple as "docker-compose up", building should be as simple as "make", checking out the code should be as simple as "git clone", etc. You shouldn't need a shitload of wiki checklists that describe how to install dependencies and how to check out all the git-directories with correct versions relative to each other.

👍for this [comment](https://news.ycombinator.com/item?id=22455368):

> 1. Working in pairs or teams. Avoid solo people working on projects.

👍for this [comment](https://news.ycombinator.com/item?id=22455767):

> That's also why I mostly prefer in code documentation to Confluence/wiki documentation, because the time/change relationship between code and wiki is much harder to comprehend.

👍for this [comment](https://news.ycombinator.com/item?id=22455640):

>  A trick I've used effectively is to have a "doc of docs" - a document that tells you where all the other documents for a project or team live.
> …
> It's a universal truth that documentation for projects and teams ends up scattered in many different places. A doc-of-docs is a lightweight technique that can really help here.

👍for this [comment](https://news.ycombinator.com/item?id=22454980):

> A per-project or per-process README would be a good first step. Ideally keep the notes/instructions as close to the place where the work will get done. It's important for someone to test the instructions in the README on a new machine --- 9 out of 10 times you'll find a step about authentication or some system dependency was not documented. Credentials are extra tricky, so you'll have to think extra hard how to make that work (e.g. some sort of central key store, shared password manager, or ENV vars that need to be defined so you avoid putting any sensitive info in the README).
>
> For something even better than a README, you could document the steps of a technical procedure in a Makefile (or Fabfile) that your colleagues can run. It's important to keep the scripts readable and stupid (as opposed to abstract and powerful like ansible), so that people can read the steps. Some people refer to this as "runnable documentation." 

👍👍👍for this [comment](https://news.ycombinator.com/item?id=22455653):

> Every commit should combine:
>
> - The code change itself
> - Tests that demonstrate that the change works as expected
> - Updated documentation relevant to that change (documentation should live in the same repo as the code to support this)
> - A link to the ticket/issue that discusses the change
>
> If you use a code review system such as GitHub pull requests or Phabricator you can enforce this kind of commit culturally - in your review point out that the test is missing or the documentation hasn't been updated or there's no link to an issue.
>
> I like building pull requests up from several commits and then using the "Squash and merge" option to merge them into a single commit to master that includes all of the above.
> 
> Doing this is great for institutional knowledge, because "git blame" can always lead you to a comprehensive explanation of the change, including a link to the underlying ticket where the change was originally requested and discussed. 

👍for this [comment](https://news.ycombinator.com/vote?id=22455322&how=un&auth=560159c8470c6be47dd707e8f70bd6b1b8f1a811&goto=item%3Fid%3D22454333#22455322):

> I've struggled with this personally at our company. A sibling comment mentioned a README for each project/process. That's definitely a solid start for building this up from nothing. Copy open source project README files:
>
> 1) what is it? (A web project, an automation script, an ansible deployment repo?)
>
> 2) what dependencies do I need to run it? (Make, NPM, Java 1.8?)
>
> 3) how do I run it? (docker-compose up? make && ./a.out?)
>
> We started with this. Then for the bigger projects/monorepos, we started adding README files in relevant subfolders.
>
> Recently I've been converting these README files in the larger projects into mkdocs subfolders that get hosted in our repository tooling (GitHub/GitLab pages).
>
> Start small. Go slow (if it's institutionally difficult). Build up to more complexity as you get more written material to work with.
>
> I've started creating an "index" project, that links to all the projects that have documentation.
>
> And finally, focus on the pain points first. One of our monorepos was fiendishly difficult to deploy correctly, either locally or in a test / production environment. The very first tutorial I wrote was setting up that environment in a step-by-step, repeatable manner, and it's by far the most oft-used documentation we have. With that out of the way, I can focus more on the esoteric details (and, yes, unfortunately, it's a bit of a thankless, "skunk works" project, but it's worth it) 

🤔🤔🤔 [comment](https://news.ycombinator.com/item?id=22455718)

> Spending hours updating your Notion or Confluence is busy-work and will be incomplete and eventually become stale anyway.
>
> Try speaking to people in real life. It's not that hard. 