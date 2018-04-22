# Media

Inherits `Object`.

 - `id` - "http://u-wave.example/as/media/MEDIA-ID"
 - `type` - "https://u-wave.net/ns#Media"
 - `published` - Datetime at which the media was created.
 - `image` - The thumbnail [Image](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-image).
 - `url` - A [Link](https://www.w3.org/TR/activitystreams-vocabulary/#dfn-link) or string URI to the media source URL.
   eg. "https://www.youtube.com/watch?v=MOUzH1K3h9U"
 - `duration` - Duration of the media; determines the maximum value for `endSeconds`.
 - `artist` - Name of the artist.
 - `title` - Title of the item.
 - `startSeconds` - Start playing at this many seconds from the start of the media.
 - `endSeconds` - Stop playing at this many seconds from the start of the media.
