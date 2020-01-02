# Servers Checklist


## Security

### Authentication

- [ ] Requires secure password.
	+ [ ] Length > 8.

### File System

- [ ] `~/.ssh/` has permission 700 for each user.
	+ `chmod 700 ~/.ssh/`
- [ ] `~/.ssh/authorized_keys` has permission 600 for each user.
	+ `chmod 600 ~/.ssh/authorized_keys`
