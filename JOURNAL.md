# 1. Schematic Design

> ⏱️ **Time Logged:** 2 Hours

I worked on creating the schematic for my macroboard. One challenge I ran into was making sure all of the components were connected correctly while also keeping the design organized. Initially, I kept getting ERC errors because of a few missing connections and incorrectly configured nets. Rather than randomly changing things, I went through each error one by one and traced the issue back to its source. This helped me better understand how the different components interacted with each other. After several revisions and checks, I was able to eliminate all ERC errors and complete a schematic that I was confident would work.

---

# 2. PCB Layout & Routing

> ⏱️ **Time Logged:** 2.5 Hours

I worked on properly laying out all the components of my macroboard and routing them. This ended up being more difficult than I originally expected because there were a large number of ratsnest lines in a relatively small amount of space. My first layout placed some traces too close to the mounting holes, which could have made the board more vulnerable to damage during assembly. I ended up moving several components and rerouting sections of the board to create more clearance while still keeping the design compact. This process taught me that PCB design is often about balancing competing constraints rather than finding a perfect solution. Overall, I am happy with the end result.

---

# 3. Bottom Case Design

> ⏱️ **Time Logged:** 1.75 Hours

I created a 3D model for the bottom case which will house my PCB. While the design itself was fairly straightforward, getting the dimensions correct required more attention than I expected. I had to account for PCB thickness, standoff placement, screw clearances, and the tolerances of 3D printing. During the design process I realized that a few measurements that worked digitally would likely be too tight once printed, so I increased clearances in several areas. Overall, I am happy with the end result.

---

# 4. Top Case Design

> ⏱️ **Time Logged:** 1 Hour

I created the top case for my macroboard. This was relatively easy since the outer dimensions were based on the bottom case. The main challenge was ensuring that the switch cutouts aligned correctly with the PCB and that there was enough room for the switches to sit properly. I double-checked measurements against both the PCB and the keyboard plate before finalizing the design.

---

# 5. Assembly Creation

> ⏱️ **Time Logged:** 45 Minutes

I created the assembly file for my macroboard.

This was not as painstaking because most of the work involved combining the different 3D files and imported components into a single model. However, the assembly helped me catch a few small alignment issues that were less obvious when looking at each part individually. Being able to verify fitment before manufacturing gave me more confidence in the final design.

---

# 6. Firmware Development

> ⏱️ **Time Logged:** 1.5 Hours

I coded the firmware for my macroboard. Since I already knew Python, learning the programming side was not too difficult. However, I was completely new to KMK and initially struggled to understand how layers, keymaps, and hardware definitions were structured. I spent time reading documentation and watching tutorials before experimenting with small test configurations. Once I understood the framework, development became much faster. This experience showed me the importance of learning how to navigate technical documentation independently when working with unfamiliar tools.

---

# 7. Parts Sourcing

> ⏱️ **Time Logged:** 2.5 Hours

I sourced the parts for my macroboard. I originally expected this to be one of the easiest parts of the project, but it ended up taking much longer than anticipated. Many components were either out of stock, sold in larger quantities than I needed, or had shipping costs that significantly increased the overall price. I compared multiple vendors and evaluated tradeoffs between cost, quality, and delivery time before finalizing my selections. This process gave me a better appreciation for the logistical side of hardware development.

---

# 8. GitHub Repository & Documentation

> ⏱️ **Time Logged:** 30 Minutes

I uploaded all of my files to my GitHub repository and created a README for final submission.

Although this was one of the shorter tasks, I wanted the project to be easy for someone else to understand and reproduce. Organizing files, documenting the design process, and including relevant resources helped make the project more accessible and complete.

---

# Reflection

I am immensely grateful for the opportunity to develop a hardware project that integrated both electrical and software engineering. I started this project because I wanted to create something useful for myself rather than simply following a tutorial. Throughout the process, I learned that building hardware involves much more iteration than I initially expected. Whether it was resolving ERC errors, rerouting traces, adjusting mechanical tolerances, or learning a new firmware framework, each challenge required a different approach to problem-solving.

Beyond the technical skills, I gained experience working through uncertainty and debugging issues that did not have obvious solutions. The project exposed me to tools and workflows used throughout the electronics industry and gave me a greater appreciation for the engineering process from concept to implementation. Most importantly, it allowed me to transform an idea into a tangible product that I am genuinely proud of.
