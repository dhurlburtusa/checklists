# Web Servers Checklist


## General

- A CDN or the web server itself is handling static content.
  + That is, no app or app server is serving static content. These should be handling dynamic content.


## Security

### File System

- [ ] `~/.ssh/` has permission 700 for each user.
	+ `chmod 700 ~/.ssh/`
- [ ] `~/.ssh/authorized_keys` has permission 600 for each user.
	+ `chmod 600 ~/.ssh/authorized_keys`
