# Servers Checklist


## General

- A CDN or the web server itself is handling static content.
  + That is, no app or app server is serving static content. These should be handling dynamic content.


## Security

### File System

- [ ] `~/.ssh/` has permission 700 for each user.
	+ `chmod 700 ~/.ssh/`
- [ ] `~/.ssh/authorized_keys` has permission 600 for each user.
	+ `chmod 600 ~/.ssh/authorized_keys`

### HTTP

- [ ] Web server is responding with appropriate `Strict-Transport-Security` HTTP header.
	+ See https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security.
