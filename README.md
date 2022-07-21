# Repro

```bash
$ npm i
$ npm t
```

The test will fail, but should produce the warning from Babel:

```
$ npm t

> jest-coverage-babel-warning-repro@1.0.0 test
> jest --clearCache && rm -rf coverage && cp node_modules/@gathertown/gather-game-common/src/generated_DO_NOT_TOUCH/events.ts ./veryLargeFile.ts && jest --coverage

Cleared /private/var/folders/cj/mqcsfk9s7l7fwkx8c1dwpsnc0000gn/T/jest_dx
watchman warning:  Recrawled this watch 3 times, most recently because:
MustScanSubDirs UserDroppedTo resolve, please review the information on
https://facebook.github.io/watchman/docs/troubleshooting.html#recrawl
To clear this warning, run:
`watchman watch-del '/Users/andrew/Projects/jest-coverage-babel-warning-repro' ; watchman watch-project '/Users/andrew/Projects/jest-coverage-babel-warning-repro'`

ts-jest[config] (WARN) message TS151001: If you have issues related to imports, you should consider setting `esModuleInterop` to `true` in your TypeScript configuration file (usually `tsconfig.json`). See https://blogs.msdn.microsoft.com/typescript/2018/01/31/announcing-typescript-2-7/#easier-ecmascript-module-interoperability for more information.

[BABEL] Note: The code generator has deoptimised the styling of /Users/andrew/Projects/jest-coverage-babel-warning-repro/veryLargeFile.ts as it exceeds the max of 500KB.
```