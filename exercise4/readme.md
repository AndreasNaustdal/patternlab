# Exercise 4 – Including patterns in one another

To include one pattern within another, for example to create a molecule from several atoms, you can use the default include syntax from Mustache.

The shorthand syntax uses the following format:
```
{{> [patternType]-[patternName] }}
```
For example, to include the following pattern in a molecule:
```
00-atoms/images/landscape-16x9.mustache
```
The shorthand include syntax would be:
```
{{> atoms-landscape-16x9 }}
```
The pattern type matches the top-level folder and is `atoms`. The pattern name matches the template file and is `landscape-16x9`. Any digits used for ordering are dropped from both the pattern type and pattern name. Pattern subtypes are never a part of the shorthand include syntax. This way patterns can be re-organized within a pattern type and/or by using digits without needing to change your pattern includes.
