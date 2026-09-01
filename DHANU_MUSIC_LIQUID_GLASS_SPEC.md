# Dhanu Music — Liquid Glass Design System

## Product identity
- App name: **Dhanu Music**
- Visual direction: premium dark-first Liquid Glass
- Principle: **The music is the content. The interface should disappear into the experience.**
- Keep the existing playback, offline, lyrics, recommendation, and discovery capabilities intact.

## Design tokens
- Background: near-black / graphite surfaces
- Glass surfaces: translucent white/graphite overlays with backdrop blur
- Corner radius: 20–32dp for primary surfaces; 14–18dp for compact controls
- Borders: subtle 1dp translucent highlight, never heavy outlines
- Shadows: soft depth only
- Typography: clean modern sans-serif with strong hierarchy
- Accent: dynamically derived from the current album artwork
- Motion: spring-based transitions, short fades, scale/blur interpolation

## Primary surfaces
1. Home: greeting, search/profile actions, Recently Played, Quick Picks, Made For You, Trending, New Releases, Your Mixes.
2. Search: instant suggestions, history, trending searches, filter chips, glass result groups.
3. Now Playing: large artwork, dynamic blurred backdrop, metadata, progress, transport controls, queue, lyrics, favorite, shuffle/repeat, and audio/video switch.
4. Mini Player: floating glass capsule above navigation; expands into Now Playing.
5. Library: Liked Songs, Downloads, Albums, Artists, Playlists, Videos with sorting.
6. Queue: draggable glass list with Play Next, Add to Queue, reorder and remove.
7. Downloads: songs/albums/playlists/videos, progress, pause/resume/cancel/delete, storage usage.
8. Lyrics: synchronized scrolling, current-line emphasis, full-screen glass overlay.
9. Settings: Playback, Downloads, Appearance, Data and accessibility controls.

## Playback requirements
- Preserve playback position when switching audio/video.
- Preserve queue, volume and playback state.
- Maintain background playback and lock-screen/media controls.
- Crossfade options: Off, 1s, 2s, 3s, 5s, 8s, 10s.
- Keep gapless playback where supported.

## Dynamic artwork
- Extract dominant/secondary colors from album artwork.
- Tint blurred background and selected glass highlights subtly.
- Do not allow accent colors to reduce text contrast.
- Animate color changes smoothly when the track changes.

## Motion and interaction
- Prefer spring motion for expansion/collapse and navigation.
- Use subtle haptics where supported.
- Support swipe gestures for queue/player interactions.
- Keep animations lightweight and target smooth 60fps behavior where hardware permits.
- Respect reduced-motion/accessibility preferences.

## Implementation guardrails
- This specification is additive: do not remove existing working playback/download/lyrics functionality merely to change visuals.
- Do not copy Apple's exact layouts, icons, assets, or proprietary visual implementation. Use the Liquid Glass concept as inspiration while keeping Dhanu Music's visual identity original.
- Keep streaming/content usage compliant with the source service's terms and user rights.
