USThing Server Migration - Endpoint Changes
===
# Testing Env
In testing phrase, `test` hostname should be added in front of `usthing.xyz`
e.g. `api.usthing.xyz` => `api.test.usthing.xyz`
e.g. `www.usthing.xyz` => `www.test.usthing.xyz`

# RestDB

The endpoint/token should remain the same, but please verify whether all resourced are accessible/correct on the test server


# Existing Node APIs
These endpoints will be redirected automatically, but should still be updated in next release.

| API | Before | After |
| -------- | -------- | -------- |
| 2FA | api.usthing.xyz/node/2FA | 2fa.api.usthing.xyz |
| Booking | api.usthing.xyz/node/Booking | booking.api.usthing.xyz |
| EMS-Email | api.usthing.xyz/node/ems-email | ems-email.api.usthing.xyz |
| LoginCAS | api.usthing.xyz/node/LoginCAS | logincas.api.usthing.xyz |
| Phonebook | api.usthing.xyz/node/Phonebook | phonebook.api.usthing.xyz |

# New Node APIs
These APIs are for replacing PHP counterparts, methods/responses could be different from existing ones and should be switched manually.

| API | Old | New |
| -------- | -------- | -------- |
| Directory | api.usthing.xyz/Directory/api.php | directory.api.usthing.xyz |
| LoginCAS | api.usthing.xyz/LoginCAS.php | logincas.api.usthing.xyz |

# Websites

These endpoints will be redirected automatically, but should still be updated in next release.

| Site | Old | New |
| -------- | -------- | -------- |
| Common Core Search | usthing.xyz/cc | ccsearch.usthing.xyz |
