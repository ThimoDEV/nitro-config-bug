# This is a repor for the nitro config issue

- Steps to reproduce: 

- Run bun dev
- Go to nitro.config.ts
- Turn on autosave in Cursor or vscode
- Remove the: " character on line 5 so the code becomes:  preset: "vercel
- Detect that nitro crashes with one of below errors



## On pnpm we get: 

node:internal/process/promises:394
    triggerUncaughtException(err, true /* fromPromise */);
    ^

[Error: ParseError: D:\: Unterminated string constant.
 D:/Github repos/Personal/nitro-config-bug/nitro.config.ts:5:10]

Node.js v22.14.0

## On bun we get: 

node:internal/process/promises:394
    triggerUncaughtException(err, true /* fromPromise */);
    ^

[Error: ParseError: D:\: Unterminated string constant.
 D:/Github repos/Personal/nitro-config-bug/nitro.config.ts:5:10]

Node.js v22.14.0
error: script "dev" exited with code 1