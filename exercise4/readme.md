# Exercise 4a – Using pattern parameters

By now you've hopefully seen how you can reference variables and their values in
your patterns.

Within any pattern you can reference variables
present in `data.json`, but when including the pattern in another,
we get the option to add or override those variables: Pattern parameters.

This is a simple mechanism with a reach limited to the included pattern alone
(i.e. it does not reach patterns included in the included, unless the included
includes another with it's own parameters... Get it? :D).

A typical use-case could be to include several button atoms in, say, a toolbar
molecule. The buttons would look the same and have the same markup (and thus
be the same atom), but the `{{label}}` on the button would need to be different for each.

Example:
```
{{> [patternType]-[patternName](variable: value) }}
```

### Modify `header.mustache` to make breadcrumbs optional
Find the line of code that includes `molecules-breadcrumb` and wrap it in...
```
{{#breadcrumbs}}
...
{{/breadcrumbs}}
```

### Include the header in both `templates`
...but only show breadcrumbs on templates _other than_ the homepage by passing
in the appropriate variable: `breadcrumbs: [true|false]`.


# Exercise 4b - Using `{{styleModifier}}`

styleModifier is a commonly used predefined parameter slightly different syntax,
but aside from that it works just like any other pattern parameter:
- You need to define where to use it in the `.mustache` file, and
- it will only be available to the first level of includes.

Example include:
```
{{> [patternType]-[patternName]:mypattern--dark }}
```
Usage in the included:
```
<div class="mypattern {{styleModifier}}">
...
</div>
```
