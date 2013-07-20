nginx-webfinger
===============

A WebFinger resource for nginx (compatible with [draft-ietf-appsawg-webfinger-14](http://tools.ietf.org/html/draft-ietf-appsawg-webfinger-14)).

To serve the files with the right `Content-Type`, add `application/json json;` to `/etc/nginx/mime.types`. Optionally, add `application/json` to `charset_types` if you want to specify the charset in the `Content-Type`.

Note that nginx doesn't decode URL parameters, so the file names have to be URL encoded as well: `?resource=acct%3Abob%40example.com` will look for a file called `/profiles/acct%3Abob%40example.com.json`. I suggest symlinks as a workaround to accept unencoded resource parameters.
