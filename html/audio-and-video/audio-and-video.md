## HTML Audio and Video

### `<video>` — Video player element

- The `<video>` element is used to embed video content natively on a webpage.
- It acts as a container for video streams or source files.
- It requires attributes to show playback controls or change playback behaviors.

### `<audio>` — Audio player element

- The `<audio>` element is used to embed sound files natively on a webpage.
- It creates a standard audio player interface for music, podcasts, or sound clips.
- Like the video tag, it uses simple attributes to control the user interface.

### `<source>` — Media source element

- The `<source>` element lives inside `<video>` or `<audio>` tags.
- It specifies the path (`src`) and the file type (`type`) of the media asset.
- You can list multiple `<source>` tags so the browser can choose the first format it supports.

### Special Attributes

- `controls` — Displays the native browser interface buttons like play, pause, volume, and fullscreen.
- `autoplay` — Starts playing the video or audio file automatically as soon as the page loads.
- `muted` — Silences the audio track by default (Modern browsers require this for `autoplay` to work).
- `loop` — Makes the media automatically restart from the beginning whenever it reaches the end.
- `poster=""` — Sets a temporary thumbnail image to display before the user clicks the play button.
- `preload=""` — Controls how much data downloads on page load (`none` for no data, `metadata` for file length only, `auto` for full download).

### Small differences

- `<video>` requires width or height attributes to control its size on screen, while `<audio>` has a fixed layout size.
- `src` can be placed directly on the main tag for simple files, but using nested `<source>` tags is safer for cross-browser support.
- `autoplay` works on audio tags freely, but browsers completely block video `autoplay` unless the `muted` attribute is also active.
