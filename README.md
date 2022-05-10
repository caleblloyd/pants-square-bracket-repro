# pants square bracket bug

`files()` fails when there are square brackets in the filename

to reproduce - run `./pants package ::`

```
22:15:10.35 [WARN] Unmatched glob from test/[test].txt:files's `source` field: "test/[test].txt"

Do the file(s) exist? If so, check if the file(s) are in your `.gitignore` or the global `pants_ignore` option, which may result in Pants not being able to see the file(s) even though they exist on disk. Refer to https://www.pantsbuild.org/v2.11/docs/troubleshooting#pants-cannot-find-a-file-in-your-project.
22:15:10.35 [ERROR] 1 Exception encountered:

  InvalidFieldException: The 'source' field in target test/[test].txt:files must have 1 file, but it had 0 files.
```