# Contributing to OpenSourcePractice

This guide explains how we work in this repository. Every change follows the same path:

**issue → branch → commit → pull request → review → merge**

## 1. Select an issue

1. Open the [Issues](https://github.com/kbexultan/OpenSourcePractice/issues) tab.
2. Choose an open issue that has no assignee, or one that is already assigned to you.
3. Read the description. If something is unclear, ask in the issue comments before you start.
4. Assign the issue to yourself (**Assignees → assign yourself**), so that two people do not work on the same thing.

Do not start work without an issue. If you want to add something new, create an issue first.

## 2. Create a branch

Never commit directly to `main`. Every issue gets its own branch, named `<issue number>-<short description>`, for example `6-add-contributing-guide`.

The easiest way is to create the branch from the issue page: **Development → Create a branch**. GitHub links the branch to the issue automatically.

Or create it in the terminal, starting from the latest `main`:

```bash
git checkout main
git pull
git checkout -b 6-add-contributing-guide
```

## 3. Write a commit message

Use this format:

```
<type>: <what you did> (#<issue number>)
```

- **type** is `feat` (new feature), `fix` (bug fix) or `docs` (documentation)
- write in the imperative mood: "add", not "added" or "adds"
- keep the first line short (under 72 characters)
- one commit = one logical change

### Example of a good commit message

```
docs: add contributing guide (#6)
```

It is good because it says what kind of change it is (`docs`), what exactly was done, and which issue it belongs to. If you need to explain more, add a blank line and a short description:

```
docs: add contributing guide (#6)

Explain how to select an issue, create a branch, write commit
messages and open a pull request.
```

Bad examples: `update`, `fix`, `changes`, `final version 2`. They do not tell anyone what was changed.

## 4. Create a pull request

1. Push your branch:

   ```bash
   git push -u origin 6-add-contributing-guide
   ```

2. On GitHub, click **Compare & pull request**. Check that the base branch is `main`.
3. Write a clear title and a short description that answers two questions: *What was changed?* and *Why is it needed?*
4. Add `Closes #N` to the description, where `N` is the issue number:

   ```
   Closes #6
   ```

   This links the pull request to the issue. When the pull request is merged into `main`, GitHub closes the issue automatically.

5. Under **Reviewers**, choose a teammate.

## 5. Review and merge

- Another team member must review the pull request. Do not merge your own pull request without an approval.
- The reviewer leaves at least one meaningful comment and chooses **Approve** or **Request changes**. Review is quality control, not personal criticism.
- If changes are requested, push new commits to the same branch. The pull request updates automatically.
- After approval, the pull request is merged into `main` and the branch is deleted.
