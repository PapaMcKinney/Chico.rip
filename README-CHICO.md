# Chico.rip memorial refresh (draft)

This project intentionally keeps the original public memorial message exactly as written: **In Loving Memory of Chico the Cat**. It references the existing `IMG_3714.JPEG` and original audio file; neither source asset is replaced, deleted, or re-encoded.

## Adding photos to the slideshow

1. Add the selected Chico images into a `photos/` folder in the site repository (JPEG, PNG or WebP). Codex or the GitHub upload interface can do this.
2. Add an entry for each photo in `photos.json`, after the first original-photo entry:

```json
{
  "src": "photos/chico-playing.jpg",
  "alt": "Chico playing with his favorite toy",
  "caption": "Playtime"
}
```

Use valid JSON: separate entries with commas. Keep the original photo first. New images will cycle approximately every 7 seconds and visitors can go forward/back or choose a photo directly. If only one photo is listed, the original image is still displayed and navigation is hidden.

This is a static memorial website, not a photo-upload system. Adding photos for all visitors requires committing the image files and updating `photos.json`; visitors cannot upload photos from the public site. A private photo-management interface could be added later.

## Music

The existing audio is set to `autoplay` and `loop`. Modern browsers, including iPhone Safari, often prevent audio from starting automatically with sound. The site attempts playback and offers an accessible **Play music** button when autoplay is blocked. Once started, the audio loops. Check usage rights for the existing music file before distributing it further.

## Publishing

Do **not** change the `CNAME` file. Preview the branch and merge only after approving the design. The live root `chico.rip` may be published automatically from GitHub's `main` branch if GitHub Pages is enabled, so don't push the draft to main without approval.