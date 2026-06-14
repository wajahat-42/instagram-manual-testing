# Test Cases — Login Page (instagram.com)

| ID    | Summary                        | Steps | Expected Result | Actual Result | Status  |
|-------|-------------------------------|-------|-----------------|---------------|---------|
| TC-01 | Valid login                   | Enter valid username + password, click Login | Redirected to home feed | Redirected to home feed | ✅ Pass |
| TC-02 | Invalid username              | Enter invalid username + valid password | Error message appears | "The username you entered doesn't belong to an account." | ✅ Pass |
| TC-03 | Invalid password              | Enter valid username + invalid password | Error message appears | "Sorry, your password was incorrect." | ✅ Pass |
| TC-04 | Empty username field          | Leave username empty, enter password, click Login | "Username is required" error | Login button stays disabled | ✅ Pass |
| TC-05 | Empty password field          | Enter username, leave password empty, click Login | "Password is required" error | Login button stays disabled | ✅ Pass |
| TC-06 | Special characters in credentials | Enter user@name and P@ssw0rd! | Login or appropriate error | Username field rejects @ at field level | ⚠️ Partial |
| TC-07 | Maximum length input          | Enter 255-char username + password | Login or error | Field capped at 30 chars; error shown | ✅ Pass |
| TC-08 | Case sensitivity               | Enter USERNAME for account "username" | Fails if case-sensitive | Login succeeds (case-insensitive) | ✅ Pass |
| TC-09 | Forgot password link          | Click "Forgot password?" | Redirected to recovery page | Redirected to /accounts/password/reset/ | ✅ Pass |
| TC-10 | Remember Me functionality     | Check Remember Me, login, reopen browser | Auto logged in | Checkbox doesn't exist on Instagram | ❌ Fail |
