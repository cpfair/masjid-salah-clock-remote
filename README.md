# Systems Integration Masjid Salah Time Clock Replacement Remote
If your masjid is like mine, your masjid just had a momentary panic over the disappearance of this remote control:

![IMG_0503](https://github.com/user-attachments/assets/43eea01b-087b-4a92-a7af-10f5fdd7e2b5)


It's the only way to update the times on prayer time clocks (aka "panels") like this, from [Systems Engineering (aka Systems Integration)](https://www.systemsengineering.com.pk/):

<img width="250" height="250" alt="image" src="https://github.com/user-attachments/assets/be9b25d6-9023-4737-b154-a2b825a9e7b2" />

You can, of course, buy a replacement remote. But what other options are there?

## Repurpose another remote
The official Systems Engineering remote uses a standard infrared protocol (RC5), also used by regular TV remotes. This means you might already have a compatible remote in your house - you just need to find which button is which. You can also try with remotes for other A/V devices, especially Phillips devices.

Here is a table of what keys might correspond with the official remote's keys:

| Official Remote |Try this button...|
|--|--|
| Unlock | 	`Ext. Input`, `AV`, `Source` |
| + | `Volume Up` |
| - | `Volume Down` |
| Set | `Ok`, `Enter` |
| Exit | `Power`, `On` |
| Menu | `Menu` |
| Hijri | `3` (digit) |
| Time | `5` (digit) |
| Iqama | `7` (digit) |
| City | `9` (digit) |

## Make your own remote

The following is a table of RC5 remote codes captured from the official remote. You can enter these into certain "universal remote" applications, or program them into an Arduino or other microcontroller. If you don't feel like building a complete remote from scratch, you could set up a simple Arduino IR sender, then use a "learning" universal remote to capture each of the button codes, giving you a proper physical remote.

| Official Remote | RC5 Address | RC5 Command |
|--|--|--|
| Unlock | 0x00 | 0x38 |
| + | 0x00 | 0x20 (upper) or 0x21 (lower) |
| - | 0x00 | 0x10 (right) or 0x11 (left) |
| Set | 0x00 | 0x25 |
| Exit | 0x00 | 0x0C (both buttons) |
| Menu | 0x00 | 0x3B |
| Hijri | 0x00 | 0x03 |
| Time | 0x00 | 0x05 |
| Iqama | 0x00 | 0x07 |
| City | 0x00 | 0x09 |
