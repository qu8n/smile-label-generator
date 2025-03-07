# A descriptive title

Briefly describe changes proposed in this pull request:
- a
- b 

---
## Troubleshooting

Fix # (see https://help.github.com/en/articles/closing-issues-using-keywords)

**Expected behavior**

**Actual behavior**

**Logs, error output, or stacktrace**

**Steps to reproduce the behavior**

**Tasks**

Include specific tasks in the order they need to be done in. Include links to specific lines of code where the task should happen at. 

- [ ] task 1
- [ ] task 2
- [ ] task 3

---
## Crossing T's and dotting I's

Please follow these checklists to help prevent any unexpected issues from being introduced by the changes in this pull request. If an item does not apply then indicate so by surrounding the line item with `~~` to strikethrough the text. See [basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) for more information.

### I. Data model checklist
Please follow these checks if any changes were made to any classes in the web, service, or persistence layers.

**Code checks:**
- [ ] Unit tests were updated in relation to updates to the mocked test data.

### II. Message handlers checklist:
- [ ] Changes introduced affect the workflow of incoming messages.
- [ ] Messages are following the expected workflow when published to the topic(s) changed or introduced in this pull request.

Please describe how the workflow and messaging was tested/simulated:

**Describe your testing environment:**

- NATS [local, local docker, dev server, production]
- Neo4j [local, local docker, dev server, production]
- SMILE Server [local, local docker, dev server, production]
- Message publishing simulation [nats cli, docker nats cli, smile publisher tool, other (describe below)]

Other: [insert details on how messages were published or simulated for testing]

### II. Configuration and/or permissions checklist:
- [ ] New topics were introduced.
- [ ] The topics and appropriate permissions were updated in [smile-configuration](https://github.mskcc.org/cmo/smile-configuration).
- [ ] If applicable, a new account was set up and the account credentials and keys are checked into [smile-configuration](https://github.mskcc.org/cmo/smile-configuration).
- [ ] Account credentials and keys were shared with the appropriate parties.

---
### Screenshots

---
### General checklist:
- [ ] All requested changes and comments have been resolved.
- [ ] The commit log is comprehensible. It follows [7 rules of great commit messages](http://chris.beams.io/posts/git-commit/). For most PRs a single commit should suffice, in some cases multiple topical commits can be useful. During review it is ok to see tiny commits (e.g. Fix reviewer comments), but right before the code gets merged to master or rc branch, any such commits should be squashed since they are useless to the other developers. Definitely avoid [merge commits, use rebase instead.](http://nathanleclaire.com/blog/2014/09/14/dont-be-scared-of-git-rebase/)
