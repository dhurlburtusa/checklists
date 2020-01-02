# Project Requirements Checklist

## Authentication

- [ ] Allow session invalidation before access token expires?
	+ If session invalidation is allowed, then JWT will indicate otherwise before the expiration time. May need to use a different strategy or at least not use the token's expiration time to assume the user is still authenticated.
