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
The outline is loosely based on the demo provided. I took a look at what components were shown, but had issues running the playground version. As a result, I did not find out what happens when a user intereacts with some features. These features are labeled as what I dubbed "Advanced Features". 

The outline is organized in the customer journey where a user will start by loading a memory dump, downloading it, then inspecting the memory dump to identify an issue. Next, I decided to explain the Threads panel as that was the high-level overview of the memory dump. 

After threads, I did not have a name for the left panel, so I called it the Issues Panel Following the demo flow, the engineer explains in low-level what the issue is from looking at the panel, so I included a section for examples of issues.

Before closing, I wanted to include a soft CTA to promote usage. This came as collaborative features, such as commenting on an issue. I did not cover merging an issue since it was outside of the red outlined box, 

Finally, I added Advanced features as  areas that I lacked information on and weren't discussed in the demo. Due to this, I assumed it's for technical experts and could be a separate page of it's own, focusing on logging (Recent traces, logs panel, and Memory viewer).

### Part Two
TBD

## Documentation Improvements

### Style Improvements

- Docs Naming. Instead of "Inspecting an Issue", use "Inspect Issue" because it's shorter and doesn't imply a tense. This makes it more accessible and simpler for future i18n efforts.
- Inspecting an Issue is a large piece of work, breaking it down into sub components like in Issues & Traces would benefit the readability. These sub components would match the H2's I put down in the outline.

### Technical Improvements
- Link to other pages where applicable.
- Add anchors to local contents.
- Add [keywords](https://docusaurus.io/docs/seo) front matter in order to build up SEO.

### Maybe?
- Create a new post under `blog/` using the existing filename conventions. Copy the header from an existing post and give it a nice title.