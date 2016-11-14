# Exercise 3 – Including patterns in one another

## Exercise 3a – Pattern includes
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

We are now going to try to include some patterns that we have allready created into another pattern. In the `_patterns/molecules` folder, try to identify three patterns: `logo-link`, `primary-navigation` and `breadcrumbs`.

You found them? Great! Now lets put includes to the test. Find the pattern `header` in `_patterns/organisms`. Now using the the include syntax try to add the three patterns we found earlier into the header pattern.

In case you're confused about where to put the includes in `header`, don't worry, we put some comments inside the pattern to help you.

If you've stopped the `gulp serve` task at this point, start it up again on the command line. If it's already running you should be able to navigate to [http://localhost:3000/?p=organisms-header]http://localhost:3000/?p=organisms-header to witness the result of all your hard work. We now have a reasonably more functioning header.

So far we've only used includes to nest one level deep, but in theory there is no limitation to how deep the nesting goes. Lets try to take it one step further in by including our newly improved `header` pattern in a page template.

Open the `homepage` pattern within `_patterns/templates` in your text editor. As you can see, we've allready included two patterns here: `hero` and `featured`. Lets see how it looks if we include the `header pattern`

## Exercise 3b – Looping patterns with `listItems`
