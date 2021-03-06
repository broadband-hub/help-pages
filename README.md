# BroadbandHub - Help Pages

## Markdown

Here are some helpful links to understand Markdown:
- What is markdown? https://www.markdownguide.org/getting-started/
- Basic syntax - https://www.markdownguide.org/basic-syntax/
- Github specific syntax - https://guides.github.com/features/mastering-markdown/
- Online markdown editor - https://dillinger.io/


## Creating new pages
- Create a new issue
  - Navigate to the [issues page](https://github.com/broadband-hub/help-pages/issues).
  - Create a new issue with the title "New page: <page name>".
  - Add comments describing what the purpose of the page should be and/or what the contents should consist of.
  - Assign the issue to yourself and optionally anyone else who is working on help pages (except @kylerummens).
  - Add the "documentation" label.
  - Add the "BroadbandHub Help Pages - Development" project.
  - Submit the issue.
- Create .md file
  - Navigate to the `/pages` directory where you will create your page. (https://github.com/broadband-hub/help-pages/tree/main/pages)
  - Click "Add file" -> "Create new file"
  - Name the file in lower-case, separated by hyphens (-), with the extension ".md". Example: creating-an-account.md.
  - Replacing the page title and link, start the file with the following text:
```
---
layout: page
title: Create an account
permalink: /create-an-account
---

# {{ page.title }}
<br>


... the rest of the content
```
  - Edit the file using Markdown.
  - When finished creating the Markdown, see the steps below to submit a pull request.
- Submit pull request
  - When ready to submit, name the commit "Created new page: <page name>".
  - Leave the commit description empty.
  - Leave the branch name as-is (the branch name will probably be something like "kylerummens-patch-1".
  - Click "Commit changes"
  - Now you are seeing the "Open a pull request page" with your commit title.
  - On the right, click "Request" next to "kylerummens" under "Reviewers"
  - Submit the pull request
- Link the pull request to the issue
  - Navigate back to the issue that you created
  - On the right, click on the gear icon next to "Linked pull requests" and select the pull request you just created.
- And you're done! The new page will be reviewed then pushed to production.



## Editing existing pages

## Updating the search
Run the following command to update the Algolia Search database:
```
ALGOLIA_API_KEY='your_admin_api_key' bundle exec jekyll algolia
```
## Run Jekyll in development mode
```
bundle exec jekyll serve
```
