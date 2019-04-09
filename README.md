﻿# pixelplanet.fun Bot prototype
1. git pull
2. Make sure you have nodejs
3. npm install
4. npm run build
5. npm start
6. provide
  x,
  y,
  path to picture,
  fingerprint (copied from your browser requests)

OR

Start program with parameters:

npm start -- TopLeftX TopLeftY PathToImage \[ShouldDither MachineCount MachineId ContinuousWatching DoNotOverrideColors Fingerprint]

Example:
```
npm start -- 2000 -12000 photo.png y 1 1 n 6,7,4,5
```

```
npm start -- 1100 3300 mario.png n 5 0 y none
```

### Note

Only first 3 parameters are required.

"--" here means following parameters will be passed directly to executing program.

## Parameters explained

**TopLeftX** - x coordinate to start image from. Matches top left pixel of the image (2000)

**TopLeftY** - Y coordinate to start image from. Matches top left pixel of the image (-12000)

**PathToImage** - path to an image to draw. (/home/downloads/mario.png)

**ShouldDither** - Dithering is a way to keep picture looking more "original like" with low amount of colors by adding noise to the image, recommended for photos. Without this a photo would look plain and have a very low color depth look. Enable this feature or not? (y/n)

**MachineCount** - If running on multiple machines, provide machine count X. (7) \[If using single device, use 1]

**MachineID** - If running on multiple machines, provide THIS machine's id 0-(X - 1) it's a zero based index. (0) \[If using single device, use 0]

**ContinuousWatching** - After program finishes, do you want to keep watching over the drawing for any griefings, and keep on fixing? (y/n)

**DoNotOverrideColors** - Option to specify color ids to not draw over. **Write any string if not used**. Used if you want to draw around something, ex. draw rainbow only on white color around other colored drawings. I used it to allow others to contribute live to the progress and not draw over their parts. Specifying "2,6" would ignore all white and black pixels playrs have placed. (2,3,4,5)

**Fingerprint** - Specify custom fingerprint for requests.
