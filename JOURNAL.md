# 1. Schematic Design

> ⏱️ **Time Logged:** 2 Hours

I made the schematic for the macroboard. The hardest part was making sure every component was connected correctly while keeping everything organized. At first I kept getting ERC errors because I had a few missing connections and some incorrectly configured nets. So, I went through every error one by one until I found what was causing it. After checking everything a few more times, I got rid of all the ERC errors and finished the schematic.

![Screenshot 2026-05-30 at 1.39.43 PM.png](https://cdn.hackclub.com/019e8018-4cee-74f8-b2cc-9a09ac39f19f/Screenshot%202026-05-30%20at%201.39.43%E2%80%AFPM.png)

---

# 2. PCB Layout & Routing

> ⏱️ **Time Logged:** 2.5 Hours

I laid out all of the components and routed the PCB. This took longer than I expected because there were a lot of ratsnest lines in a pretty small space. My first layout had a few traces too close to the mounting holes, so I moved some components around and rerouted parts of the board until everything had enough clearance while still keeping the board compact. I ended up changing the layout a few times before I was happy with it.

![Screenshot 2026-06-01 at 11.23.31 AM.png](https://cdn.hackclub.com/019e83ff-c74a-74b1-b365-fa3ab7e488c0/Screenshot%202026-06-01%20at%2011.23.31%E2%80%AFAM.png)
![Screenshot 2026-06-01 at 11.23.26 AM.png](https://cdn.hackclub.com/019e83ff-de84-729d-a3b9-6a9162b059ad/Screenshot%202026-06-01%20at%2011.23.26%E2%80%AFAM.png)
![Screenshot 2026-06-01 at 11.15.37 AM.png](https://cdn.hackclub.com/019e83f9-34a5-7718-a254-aedac2e83a02/Screenshot%202026-06-01%20at%2011.15.37%E2%80%AFAM.png)
![Screenshot 2026-06-01 at 11.15.42 AM.png](https://cdn.hackclub.com/019e83f9-2ced-777c-85af-b2cd794388fa/Screenshot%202026-06-01%20at%2011.15.42%E2%80%AFAM.png)

---

# 3. Bottom Case Design

> ⏱️ **Time Logged:** 1.75 Hours

I designed the bottom case. It wasn't too hard, but getting all the dimensions right took longer than I expected. I had to account for the PCB thickness, standoff placement, screw clearances, and the tolerances of 3D printing. While I was designing it, I noticed a few spots that would probably be too tight once it was printed, so I gave those areas a little more clearance before finishing it.

![Screenshot 2026-05-30 at 1.46.41 PM.png](https://cdn.hackclub.com/019e801a-5cac-75b6-a212-eadd07bfe0c8/Screenshot%202026-05-30%20at%201.46.41%E2%80%AFPM.png)

---

# 4. Top Case Design

> ⏱️ **Time Logged:** 1 Hour

I designed the top case. This part was pretty easy since the outside dimensions were already based on the bottom case. Most of my time went into making sure the switch cutouts lined up with the PCB and that the switches had enough room to fit correctly. Before I finished it, I checked all of the measurements against the PCB and keyboard plate one more time.

![Screenshot 2026-05-30 at 1.43.57 PM.png](https://cdn.hackclub.com/019e801a-cc67-70da-afe1-f29bb6068156/Screenshot%202026-05-30%20at%201.43.57%E2%80%AFPM.png)

---

# 5. Assembly Creation

> ⏱️ **Time Logged:** 45 Minutes

I created the assembly file.

This didn't take too long because most of the work was putting all of the parts together into one model. Even though it was pretty simple, it helped me catch a couple of alignment issues that I didn't notice while looking at each part by itself. It also let me make sure everything fit together before manufacturing.

![Screenshot 2026-05-30 at 3.53.38 PM.png](https://cdn.hackclub.com/019e801b-f8c5-768f-9d23-40e21bfe7f89/Screenshot%202026-05-30%20at%203.53.38%E2%80%AFPM.png)

---

# 6. Firmware Development

> ⏱️ **Time Logged:** 1.5 Hours

I wrote the firmware. Since I already knew Python, that part wasn't too hard. KMK was completely new to me though. At first I wasn't sure how layers, keymaps, and the hardware definitions worked together, so I spent some time reading the documentation, watching tutorials, and testing small examples until everything started making sense. After that, writing the rest of the firmware went a lot faster.

---

# 7. Parts Sourcing

> ⏱️ **Time Logged:** 2.5 Hours

I sourced all of the parts for the project. I thought this would be one of the easiest parts, but it ended up taking a lot longer than I expected. Some parts were out of stock, some were only sold in bigger quantities than I needed, and shipping added more to the total than I expected. I checked a few different vendors before deciding where to order everything from.

---

# 8. GitHub Repository & Documentation

> ⏱️ **Time Logged:** 30 Minutes

I uploaded all of my project files to GitHub and finished the README.

This didn't take very long, but I wanted everything to be organized and easy to follow. I cleaned up the repository, made sure everything was in the right place, and added the documentation someone would need if they wanted to build it themselves.

---

# Reflection

I started this project because I wanted to build something I'd actually use instead of just following a tutorial. It ended up taking a lot more time and revisions than I expected. I'd finish one thing, then notice something else that needed to be fixed or adjusted. That happened with the schematic, PCB, case, and firmware.

By the end of the project I had designed the PCB, made the case, wrote the firmware, sourced all of the parts, and documented everything. Seeing it go from an idea to something I could actually build made all of the extra work worth it, and I'm really happy with how it turned out.
