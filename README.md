# Bug description

On the latest **VSCode** version if you have `"typescript.preferences.importModuleSpecifier"` set to `"project-relative"` the suggested imports are from the root of the monorepo, not from the project you are in.

From my observations, it only happens with **Typescript** version lower than `5.4.x` (at least on `5.3.3` bug is still there, but on `5.4.x` it is gone).

# Steps to reproduce

1. `npm i`
1. Go to `apps/vscode-imports-bug/src/app/app.tsx`
1. Try to auto-import `NxWelcome` component
1. See it being imported from `apps/vscode-imports-bug/src/app/nx-welcome` instead of `./nx-welcome`
