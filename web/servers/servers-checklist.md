# Web Servers Checklist


## General

- [ ] A CDN or the web server itself is handling static content.
  + That is, no app or app server is serving static content. These should be handling dynamic content.


## Security

The security checks here are web server specific. Also see https://github.com/dhurlburtusa/checklists/edit/master/servers/servers-checklist.md for general server security.

### Authentication

- [ ] Requires secure password.
	+ [ ] Length > 8.
	+ [ ] Max length is typically 64 if using Bcrypt.
	+ [ ] Has password strength meter.
	+ See https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Authentication_Cheat_Sheet.md.
- [ ] Requires re-authentication for sensitive features such as updates to sensitive account information such as the user's password, email, etc.
- [ ] Uses a generic error message regardless of whether the user ID or password was incorrect, the account does not exist, or the account is locked or disabled.
- [ ] Authentication logic does not suffer from time-based attacks.
	+ See https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Authentication_Cheat_Sheet.md#authentication-and-error-messages for details.
- [ ] Password recovery process does not response with "This email address doesn't exist in our database".
- [ ] Password recovery process responds with "If that email address is in our database, we will send you an email to reset your password".
- [ ] Account creation process does not respond with "This user ID is already in use".
- [ ] Account creation process responds with "A link to activate your account has been emailed to ⟨input email address⟩".
- [ ] Brute force attack protection in place, e.g., account lockout or MFA.
- [ ] Credential stuffing attack protection in place, e.g., account lockout or MFA.
- [ ] Password spraying attack protection in place, e.g., account lockout or MFA.
- [ ] Multi-factor authentication (MFA) in place.
- [ ] Allows authentication via password recovery (aka forgotten password) functionality, even if the account is locked out.
- [ ] Uses CAPTCHA.
	+ Uses CAPTCHA only after failed login attempts.
- [ ] If security questions are used, only secure (i.e., has hard-to-guess answers) are used.
- [ ] All authentication failures are logged and reviewed.
- [ ] All password failures are logged and reviewed.
- [ ] All account lockouts are logged and reviewed.

### HTTP

- [ ] Web server is responding with appropriate `Strict-Transport-Security` HTTP header.
	+ See https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security.
