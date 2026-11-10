# DoublePixel - studio site

Privacy policies, terms and `app-ads.txt` for DoublePixel's games, served by GitHub Pages at
<https://doublepixel-studio.github.io/>.

This repository is **public on purpose**: Google Play and the App Store need a privacy policy at
a URL anyone can open, and free GitHub Pages serves only public repositories. Nothing here but
static HTML - no game code, no keys.

The rules for these pages (format, both languages, what a policy must say) are in the private
studio handbook, `doublepixel-studio/mobile-games/CLAUDE.md`, section "Legal pages".

## Adding a game

One folder per game, one page per document:

    <game-slug>/privacy-policy.html
    <game-slug>/terms.html            (if the game has terms)
    <game-slug>/delete-account.html   (if the game has accounts)
    <game-slug>/index.html            (support page, if the game has one)

then add a card to `index.html` and a row below. The URL a store has been given must never
change afterwards, so pick the folder name once and leave it alone.

## app-ads.txt

`app-ads.txt` at the root is what AdMob reads for every game whose store listing names
`https://doublepixel-studio.github.io` as its website. It must contain exactly:

    google.com, pub-8111779805371074, DIRECT, f08c47fec0942fa0

## games.json: the "More games" list in every game

`games.json` at the root is the one live list of the studio's games that every game shows in its
Settings ("More games"), with each game's icon in `games/icons/<key>.png` (square PNG, 256x256,
under 60 KB). The games read <https://doublepixel-studio.github.io/games.json> and fall back to a
copy bundled in each build, so adding, removing or changing a game here needs no game release.
Data only, never code. A platform block (`android`, `ios`) is present only while the game is live
in that store. How to edit it and how to check it afterwards: the studio repo's
`.claude/skills/more-games/SKILL.md` (`doublepixel-studio/studio`).

## Live URLs

| Game | Privacy policy | Terms |
|---|---|---|
| Toy Flyers (`com.doublepixel.toyflyers`) | <https://doublepixel-studio.github.io/toyflyers/privacy-policy.html> | <https://doublepixel-studio.github.io/toyflyers/terms.html> (support page <https://doublepixel-studio.github.io/toyflyers/>, account deletion <https://doublepixel-studio.github.io/toyflyers/delete-account.html>; Play Data safety: `play-forms/data-safety-toyflyers.csv`) |
| Gravity Bop (`com.doublepixel.gravityswitch`) | <https://doublepixel-studio.github.io/gravity-bop/privacy-policy.html> | none (support page <https://doublepixel-studio.github.io/gravity-bop/>, account deletion <https://doublepixel-studio.github.io/gravity-bop/delete-account.html>) |
| RouteBots (`com.doublepixel.routebots`) | <https://doublepixel-studio.github.io/routebots/privacy-policy.html> | none (no accounts or purchases) |

Games published before 2026-10-23 keep their pages at <https://barsagivv.github.io/arclogic-studio/>.
