# Example Subsequent Workflow Trigger

A companion example repository to
[Trigger another GitHub Workflow - without using a Personal Access Token][post].

## Demo

Prettify formats all source files on push.

1. [Fork the repository][fork]
2. [Enable actions][enable-actions] for the forked repository
3. Following the post, [Add Deploy Key to GitHub Repository][post/deploy-keys]
4. Make a change to one of the source files, e.g: add some new lines to the end
   of this file
5. Push changes to the repository

Observe the result of this Push:

1. Prettify Workflow is executed by GitHub Actions
2. Job prettifies the changed file(s)
3. Format changes are pushed back to the repository
4. Prettify Workflow is executed _again_
5. No changes are generated, Workflow terminates

[post]: https://medium.com/p/f594c21373ef
[post/deploy-keys]: https://medium.com/p/f594c21373ef#7a8c
[fork]: fork
[enable-actions]: actions
