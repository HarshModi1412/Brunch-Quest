# The Brunch Quest

A playful three-clue treasure hunt for the Senior Program Manager promotion brunch.
It is one static page (`index.html`) plus a `media/` folder, with no build step and no audio files: the background music and every sound effect are generated live in the browser.

## How the hunt works
1. Each clue tells her where to go (and has a hint button if she gets stuck).
2. At that spot she finds something, plus a keyword.
3. She types the keyword under the clue, and the next clue unlocks. After the third, she texts you the final code to get the brunch location.

## Edit the words
Open `index.html` and look for the `EDIT ME` block near the top of the script. The start-screen text, the three clues, their keywords and hints, the final code, the chai note and the wrong-keyword lines all live there.
`musicEasterEgg: false` switches off the music-box tune hidden in the background music.

To jump straight to a scene while testing, press start and add its name to the URL, for example `.../#clue2`, `#cracked3` or `#end`.

## Put it online (GitHub + Render)
1. Create a **private** GitHub repository. This folder holds personal photos, so keep the repo private.
2. Push the contents of this folder to the repository root:
   ```bash
   git init
   git add .
   git commit -m "The Brunch Quest"
   git branch -M main
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
3. In Render, choose **New > Blueprint** and pick the repository. `render.yaml` sets everything up as a free static site.
   (Or **New > Static Site**: leave the build command empty and set the publish directory to `.`)
4. Open the `onrender.com` link on a phone, turn the sound on and press start.

The page asks search engines not to index it (`robots.txt`, a `noindex` meta tag and an `X-Robots-Tag` header), but anyone who has the link can still open it.
