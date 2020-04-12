# Anarchy's contributing guide

You can help contribute to Anarchy in many ways, including

## Writing code

* Follow shell scripting best practices (e.g. as described in
[Google's shell style guide](https://google.github.io/styleguide/shell.xml))
* Try to be POSIX compliant
* Use `"${variable}"` instead of `$variable`
* Constants (and global variables) should be in `UPPER_CASE`, other variables
should be in `lower_case`
* Use single square brackets (`[ condition ]`) for conditionals
(e.g. in 'if' statements)
* Write clean and readable code
* Write comments where needed (e.g. explaining functions)
* Explain what arguments a function takes (if any)
* Use different error codes when exiting and explain when they occur
at the top of the file
* If you've created a new file or made big changes (judge this by yourself),
you can add a copyright disclaimer below the shebang and any other copyright
notices (e.g. `Copyright (C) Jane Doe <contact@jane.doe>`)
* Use the `log` function if necessary
* Always line wrap at 80 characters
* Scripts are named `setup-*` (without a `.sh` extension)
* Libraries (`lib` directory) should always have a `.sh` suffix and NO shebang
* Neither script nor libraries should be executable (their permissions are
set during compilation)
* Use shellscript to error-check your code
* Test your code before submitting a PR (unless it's a draft)

## Translating (updating existing translations)

Anarchy Linux supports a bunch of languages, most of which need maintainers.

* Make sure to use the UTF-8 encoding
* Don't change the variable names (e.g. `intro_msg=`)
* Don't remove any occurrence of `\n` or `\n\n` (new lines)
* Don't remove any special characters (e.g. `$a` or quotes)
* Don't edit variables within the text (e.g. `/dev/${DRIVE}` or `${user}`)
* Compare the finished file with english.conf
* If you intend to maintain the translation, add yourself as a maintainer
at the top of the file (example below)
* If there are existing maintainers, add yourself on a new line below theirs

```
# Maintainer: John Doe <contact@john.doe>
# Maintainer: Jane Doe <contact@jane.doe>
```

_Comparing language files to one another makes Anarchy more consistent
and easier to update in the future._

## Translating Anarchy to new languages

* Ask yourself if you're committed enough to translate the whole file
(check english.conf for size comparison - ~500 translations)
* Copy the `english.conf` file and rename it to your language's
english name (e.g. `portuguese.conf` or `spanish.conf`)
* Change the LANG variable to your language's UTF-8 locale (e.g. `sl_SI.UTF-8`)
* Read above recommendations
