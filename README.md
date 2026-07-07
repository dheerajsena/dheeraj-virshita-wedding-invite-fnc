# Dheeraj & Virshita Wedding Invite

A GitHub Pages ready static wedding invite for friends and cousins.

## Required repository structure

Upload the files exactly like this at the root of the GitHub repository:

```text
index.html
.nojekyll
README.md
frames/
  frame-01.jpg
  frame-02.jpg
  ...
  frame-65.jpg
```

Do not put `index.html` inside an extra folder. GitHub Pages needs `index.html` at the repository root.

## GitHub Pages setup

1. Open the GitHub repository.
2. Go to **Settings**.
3. Go to **Pages**.
4. Under **Build and deployment**, choose:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/root**
5. Save.

Your live link will look like:

```text
https://<your-github-username>.github.io/<repository-name>/
```

## Editable placeholders

In `index.html`, search for:

```text
[RSVP_LINK_PLACEHOLDER]
```

Replace it with the final RSVP form link when ready.

## Frame sequence notes

The internal scroll-driven sequence uses these files:

```text
frames/frame-01.jpg to frames/frame-65.jpg
```

The JavaScript config is inside `index.html`:

```js
const sequenceConfig = {
  imageArray: FRAME_IMAGES.slice(0, 65),
  frameHeight: 4300
};
```

You can adjust `frameHeight` to make the internal reel feel shorter or longer while scrolling.
