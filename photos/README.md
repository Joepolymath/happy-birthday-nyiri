# photos/

Everything visual lives here. Drop files in, then point to them from the
`CONFIG` block in `her-birthday.html` using **relative paths** like
`photos/first-date.jpg`. Nothing else in the code needs to change.

## Reveal photos

For each sealed note you want a picture on, set its `image` in `CONFIG.reveals`:

```js
{ seal: "✦", title: "The day we met", body: "…", image: "photos/first-date.jpg" }
```

- **Portrait or landscape both work.** The card keeps each photo's real shape
  (a tall portrait is capped so it can't push the note off-screen).
- She can **tap any photo to see it full-screen** — no setup needed.
- Leave `image: ""` for a note with no photo (an elegant placeholder shows).
- If a path is wrong or a file is missing, the placeholder shows instead of a
  broken image — so it's safe to wire paths up before the files are in.

## Keep it fast on her phone

She'll open this on mobile, so shrink photos before adding them:

- Resize the longest edge to **~1600px** and export **JPG at ~80% quality**.
- Aim for **under ~400 KB** per photo.
- On a Mac: open in Preview → *Tools ▸ Adjust Size* → *File ▸ Export* (JPEG,
  quality ~80%). Or use https://squoosh.app (drag in, pick MozJPEG).

## Share preview (`share-preview.jpg`)

When you send her the link, chat apps show a preview card. To give it a photo,
add a file here named exactly **`share-preview.jpg`** (about **1200 × 630 px**).
The title and description are set in the `SHARE PREVIEW` block at the top of
`her-birthday.html`. If you don't add this image, the preview just shows the
title and description with no picture — still fine.

## Finale video message (`message.mp4`)

Want to end with a short clip of you? Add an **`.mp4`** here (e.g.
`message.mp4`) and set it in `CONFIG.finale`:

```js
video: "photos/message.mp4",
poster: "photos/message-still.jpg",  // optional still shown before she taps
```

- It stays **silent until she taps play** (phones block surprise sound anyway).
- Keep it short and compress it (H.264 MP4, ~720p is plenty for a phone).
- `poster` is optional — without it, the video's first frame is used.
