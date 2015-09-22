## Output a Content Element
```typoscript
lib.footer = RECORDS
lib.footer {
    table = tt_content
    source = 45 # uid of the content element
}
```