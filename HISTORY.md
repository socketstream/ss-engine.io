History
===

0.1.1
---

- Major fix: When a socket reconnects to the server, all session channels are bound to the new socket
- Apologies for not maintaining the changelog between here and 0.0.4. This will be backdated along with git tags for each version.

0.0.4
---

- Fixed a bug where the config was not being set to a default
- Changed the default to bind to the application's browser address

0.0.3
---

- Integrated a fix asked for in [this issue](https://github.com/socketstream/socketstream/issues/309)
- Updated [engine.io](https://github.com/LearnBoost/engine.io) to 0.3.3


0.0.2
---

- Fixed [a bug where the client assumed that the app was running on port 80 or 443](https://github.com/Anephenix/ss-engine.io/issues/1)
- As a result of fixing that bug, the user can configure the ss.engine-io library's address and port.


0.0.1 
---

- Fixed a mistying in the package.json file


0.0.0 
---

- Initial version release