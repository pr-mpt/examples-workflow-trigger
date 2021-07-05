# Example Subsequent Workflow Trigger

A companion example repository to
[Trigger another GitHub Workflow - without using a Personal Access Token][post].

## Demo

Prettify all source files on push, using [Prettier][prettier].

1. [Fork the repository][fork]
2. [Enable actions][enable-actions] for the forked repository
3. Following the post, [Add Deploy Key to GitHub Repository][post/deploy-keys]
4. Make an [ugly change][prettier/quotes] to one of the files, e.g: replace 
   double quotes with single in 
   [`.github/workflows/prettify.yml`][workflows/prettify]
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
[workflows/prettify]: .github/workflows/prettify.yml
[prettier]: https://prettier.io/
[prettier-quotes]: https://prettier.io/docs/en/rationale.html#strings