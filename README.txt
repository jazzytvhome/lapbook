📔 LAPBOOK STUDIO — quick start
================================

WHAT IT IS
  A web page where you and a friend build a lapbook together: drag flap
  cards, sticky notes, text labels, and PHOTOS onto a tri-fold folder.
  - "Preview" shows the assembled folder.
  - "3D" shows a rotatable 3D model that folds (slide the Fold slider).
  - When Firebase is set up, edits sync LIVE between both of you.


RUN IT RIGHT NOW (no setup, works on this PC only)
  1. Double-click  index.html  (it opens in your browser).
  2. Add flaps/notes/text/photos, drag them around, try Preview and 3D.
     Everything is saved automatically in your browser.


TURN ON LIVE MULTIPLAYER (do this once, ~3 minutes, free)
  1. Go to  https://console.firebase.google.com  and sign in with Google.
  2. Click "Add project". Give it any name. (You can skip Analytics.)
  3. In the left menu: Build > Realtime Database > Create Database.
       - Pick any location, then choose "Start in TEST mode" > Enable.
  4. Click the gear icon (top left) > Project settings.
       - Scroll to "Your apps" > click the web icon  </>
       - Register the app (any nickname) > you'll see a "firebaseConfig".
  5. Copy the config object and paste it into index.html where it says
     window.FIREBASE_CONFIG = { ... }   (near the top of the file).
       Make sure it includes apiKey AND databaseURL.
  6. Save the file. Reopen it — the top bar should say "🟢 LIVE".


PLAY TOGETHER
  - Type the SAME room name (e.g. "dinosaurs") in the Room box, OR just
    share the page's URL — the room is in the URL after the #.
  - Each person types their name; your color tags everything you add.
  - You'll see colored dots for who's online, and edits appear instantly.


PUTTING IT ONLINE (optional, so your friend doesn't need the file)
  - You already use Vercel. Drop this folder into a Vercel project (or run
    "vercel" in this folder) and it deploys as a static site. The Firebase
    config travels with the file, so live sync keeps working.


NOTES
  - Photos are shrunk to ~700px before saving so the shared database stays
    fast. Big originals aren't uploaded full-size.
  - TEST mode Firebase rules are open to anyone with the link — fine for two
    friends, but don't put private info in it. Tighten the rules later if you
    want (Realtime Database > Rules).
