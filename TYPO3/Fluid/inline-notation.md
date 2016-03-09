# Inline Notation

## basic

```xml
<source url="{ext:generate.url(foo: 'bar', baz: qux.baz)}">
  ...
</source>
```

## piping

```xml
{namespace ext=Bash\Extension\ViewHelpers}
<source url="{ext:generate.url(foo: 'bar', baz: qux.baz) -> f:format.htmlspecialchars() -> ext:fantasy()}">
  ...
</source>
```

