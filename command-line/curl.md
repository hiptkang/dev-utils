# CURL Examples

## [Basic][1]
```sh
# use remote name and follow HTTP redirects
curl -OL $URL

# specify file name
curl -o $NAME --create-dirs $URL
```

## [Cookies][2]

```sh
# set cookie (-b, --cookie)
curl -b $AUTH_KEY=$AUTH_VALUE $URL
```

## References

- [curl manpage][1]
- [HTTP Cookies][2]

[1]: https://curl.haxx.se/docs/manpage.html
[2]: https://curl.haxx.se/docs/http-cookies.html
