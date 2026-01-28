gitignore 

Example terminal session:

```bash
%> bash git_ignore.sh | cat -e
.DS_Store$
mywork.c~$
%>
```

`nano git_ignore.sh`

`git ls-files --others --ignored --exclude-standard`

## Parameters

https://git-scm.com/docs/git-ls-files

`-o`
`--others`
Show other (i.e. untracked) files in the output

`-i`
`--ignored`
Show only ignored files in the output. Must be used with either an explicit _-c_ or _-o_. When showing files in the index (i.e. when used with _-c_), print only those files matching an exclude pattern. When showing "other" files (i.e. when used with _-o_), show only those matched by an exclude pattern. Standard ignore rules are not automatically activated; therefore, at least one of the `--exclude*` options is required.


`--exclude-standard`
Add the standard Git exclusions: .git/info/exclude, .gitignore in each directory, and the user’s global exclusion file.








