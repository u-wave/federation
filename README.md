# üWave Federation

This repository functions as a notebook and a draft for potential ways to enable server-to-server communication for üWave. The goal is to allow users to sign up for a single server, and then use that account and their playlists on other servers seamlessly.

Where possible, existing web standards should be used.

## Notes

- OAuth is probably a good way to go to share user accounts.
  - We can maybe auto-auth if you have joined a server, and join a different one via an [üWave announce server](https://github.com/u-wave/hub) in the server's UI (ref https://github.com/u-wave/web/pull/864).
  - Like mastodon we can disambiguate users by their home server. `reanna@u-wave.example` and `reanna@wlk.yt`
- [ActivityStreams](./activitystreams) could be used to share playlists, plays, user profiles.
  - POST updates you do on a different server to your home server's [ActivityPub][] inbox (but see note in next point).
- [ActivityPub][] has an `outbox` concept that seems like a nice replacement for the announce server's custom format, it could GET the outbox and receive HistoryEntry Objects. But we would not implement most other ActivityPub things so maybe there is a more focused spec that would be better suited.

## License

[CC-BY-3.0](https://creativecommons.org/licenses/by/3.0/)

[ActivityPub]: https://www.w3.org/TR/activitypub/
