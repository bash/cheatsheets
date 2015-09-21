## Rewrite a single Query Parameter

```apache
RewriteBase /
RewriteCond %{QUERY_STRING} ^(.*)a=10&b=20(.*)$
RewriteRule ^(.*)$ $1?%1a=50&b=100%2 [R=301,L]
```