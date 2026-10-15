SUPER AN BROS. - how to use
1) Open index.html in Chrome/Edge/Safari (double-click). Works offline. Phone: host the folder anywhere or AirDrop/zip it.
2) Swap sprites: replace PNGs in assets/sprites/ keeping the SAME filenames. Any size works; everything scales from idle_0.png.
   idle_0 | walk_0-9 | run_0-8 | jump_0-7 (1 up, 3 apex, 4 falling) | sleep_6 (in bed), sleep_7 (nap), sleep_8 (death)
   coffee_0 (idle w/ cup), coffee_2-3 (run w/ cup), coffee_4 (jump w/ cup)
   Optional overrides (code draws them if missing): bean, cup, book, flower, qblock, brick, ground, bed, castle
   Sprites face RIGHT. If yours face left, set facesRight:false in CONFIG.
3) Swap sounds + edit all the text (title, death messages, ending message) in the CONFIG block at the top of index.html.
Controls: arrows/WASD + Space, Shift = sprint, P = pause, M = mute (remembered). Phone: on-screen buttons.
Sounds can be listed without an extension ('sem'); it tries .mp3 then .ogg.

SOUNDS (assets/sounds/): one clip per event, list the filenames in CONFIG.sounds at the top of index.html.
  start, jump, coin, item (cup pops out), power (grab coffee), crash (coffee wears off), wake, bump, stomp, die, pit (fell in a nap trap), flower, pause, win
  Any event without a working file plays a retro beep, so you can add them one at a time.
WIN MUSIC (assets/music/): put your song there and set CONFIG.winMusic (e.g. ['ending.mp3'] or just ['ending']).
  winMusicStart = seconds to skip into the song, winMusicLoop = loop it, musicVolume = 0-1. If no song is found, the short 'win' jingle plays instead.
  The song stops when you replay, and M mutes it too.
