# Memfault Takehome Write Up

## Run the Take Home
Install dependencies:

```
$ yarn
```

Start a local webserver that will pick up most changes without restarting:

```
$ yarn start
```

Navigate to the documentation page for [Inspecting an Issue](http://localhost:3000/docs/platform/inspecting-an-issue
).

## Linter

Code is linted with prettier. To fix up files to match format, run:

```
$ ./node_modules/.bin/prettier --write path/to/file.mdx
```

There is also a [`.pre-commit-config.yaml`](`.pre-commit-config.yaml) config available. install pre-commit with `pip install pre-commit`, then install the hooks with `pre-commit install --install-hooks`. Once that's setup, the pre-commit hook will run prettier on changes!

See https://pre-commit.com/ for details.

## Takehome Content

The Takehome deliverables can be broken down into 3 parts: Outlining, Writing, and Publishing.

### Part 1: Outline "Inspecting an Issue" 
Add a new page called "Inspecting an Issue" to the docs:

1. Choose a subdirectory under `docs/platform` since it's a web app doc.

2. Name a markdown file called "inspecting-an-issue" to exactly follow the instructions.

3. Inside the doc, create an outline of what the doc contents are.

4. Add the new page to `sidebars.js`.

### Part 2: Write parts of "Inspecting an Issue"

1. Write the introductory paragraph that will introduce how to inspect an issue.

2. Write the Threads section

## Process
Any relevant important things for the reviewers to be aware of.

### Part One
The outline is organized following the customer journey, A user starts at the dashboard page and inspects high-level and low-level root causes. This could be an error with the software update, or bad code running on the device. Next, I decided to explain the Threads panel as that was how a user would dive deeper into the issue. 

After threads, I did not have a name for the left panel, so I called it the Issues Panel. My outline follows the flow of the demo, the engineer explains in low-level what the issue is from looking at the panel, so I included a section for examples of issues.

Before closing, I wanted to include a soft CTA to promote usage. This came as collaborative features, such as commenting on an issue. I did not cover merging an issue since it was outside of the red outlined box. 

Finally, I added Advanced features as areas that I lacked information on and weren't discussed in the demo. Due to this, I assumed it's for technical experts and could be a separate page of it's own or link out to an existing page, such as "Debugging Core Dumps" or "Inspecting Memory regions".

### Part Two
While writing the intro for part 2, I had access to the demo and redid some of part one to clarify what the top section was for. I wrote the intro as a high-level blueprint of what's on the Issues Dashboard/Issues Detail View and how it related back to inpecting an issue. For the threads, I focused on what was shown in the initial image given for the assignment, as a stack-trace for processes. 

For the intro, I tried to give a high-level overview of all important components in the issue details page. I focused on breaking down each section into sizable chunks. I started with an intro on why a user might be inspecting an issue, focusing on Memfault's selling point of analyzing core dumps. Next, I wrote about the usefulness of the UI/dashboard and how the page is organized in. Similarly to the outline, I ordered the items following the customer journey of looking for high-level causes and then diving deeper into low-level causes.

In the threads section, I broke down the panel into 2 sections, one focusing on the call stack, and the other on tags. The call stack is relatively straightforward so I felt that there wasn't much to say as the contents are not clickable. For both technical and non-technical users, the tags are the bread and butter of the thread section. These tags didn't have a name, so I gave them names based on their puposes. I further simplified tags by making it clear they were mutually exclusive tags, so a state tag cannot be running and blocked and a causal tag cannot be due to a stack overflow and a system interupt by user. For the selling point, I doubled down on the automated analysis shown by the Stack Overflow tag in the playground. 

To end off part 2, I included images of the product using the photos provided in the take home assignment. I added an alt text for screen readers that describes the image and followed best practices of using the ImageComponent. I ended up using relative path after some time trying to get the absolute path working. I did a file search on the repo and noticed all other image component usage for the web app is also using relative, so I chose to match it. 

### Part 3
TBD

## Documentation Improvements

### Style Improvements
- Docs Naming. Instead of "Inspecting an Issue", use "Inspect Issue" because it's shorter and doesn't imply a tense. This makes it more accessible and simpler for future i18n efforts.
- Modules. Inspecting an Issue is a large piece of work, breaking it down into sub components like in Issues & Traces would benefit the readability. These sub components would match the H2's I put down in the outline focused on explaining the UI, issue examples, and advanced features.

### Technical Improvements
- Link to other pages where applicable.
- Add [keywords](https://docusaurus.io/docs/seo) front matter in order to build up SEO.
- Improve maintainability by using absolute paths instead of relative paths for images.

### Maintainence Mentions
- I wasn't sure if there were more casual tags.

### Maybe?
- Create a new post under `blog/` using the existing filename conventions. Copy the header from an existing post and give it a nice title.