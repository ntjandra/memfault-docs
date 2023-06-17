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

3. Add the new page to `sidebars.js`.

### Part 2: Write parts of "Inspecting an Issue"

1. Write the introductory paragraph that will introduce how to inspect an issue.
2. Write the Threads section

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