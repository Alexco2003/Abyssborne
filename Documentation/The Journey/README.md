# **The Story of Abyssborne**
---

# **Motivation**

I have loved games since I was a child, and this year, I had the opportunity to channel that passion into a university project that turned into a full-fledged playable game: *Abyssborne*. At first, it was my first contact with **Unreal Engine 5**, Blueprints, and all the tools that come with it. As I learned more and gained confidence with UE5, my initial project grew into a passion. 

I made a full plan for this game, aiming to deliver a great single-player experience with the complete package: game mechanics, animations, VFX, audio, menus, enemies, environment, lighting, shadows, AI, balance changes, testing, and more. Essentially, I wanted to include as much as I could to create an enjoyable and cohesive experience for players.

Step by step, I made more changes and updates, constantly thinking about how to make the game more enjoyable. I asked myself: "What can I do more? How? Why?" These are the thoughts that run through every game developer's mind. 

It wasn’t always easy being a one-person team. This project was designed as a solo endeavor for university, and through it, I learned to appreciate the power of collaboration in game development. No one, not even me, can excel in every department required for a game. Still, I thoroughly enjoyed the process, and here we are with a solid first game of mine. 

I hope you enjoy reading this documentation about how the game came to life. A quick note: there will be spoilers ahead. Additionally, no code will be discussed in this documentation. The code is well-documented in the editor, with plenty of comments and notes. If you want to explore the code, you can find it in the repository. 

Here, we will discuss the journey of making *Abyssborne* and how everything works, from a more technical perspective. If you’re a player reading this, maybe leave this for now, enjoy the game, and come back later—the game was designed to explain everything you need to know to play. 

Let’s get to the next chapter in this story!

# **The Starting Point**

So, my first thoughts on finding an idea for this game were like this: I love story-driven games. My favorite game series is **God of War**, and you can clearly see the influence of that here. However, if I wanted to make something like "the next God of War," it would mean I needed to be an exceptional artist to create the stunning environments that games like these excel in. But I am no artist. Attempting a story-driven game with varied levels, each requiring unique artistic visions, models, and meshes, would have been a suicide mission given my time, resources, and experience.

### Finding a Feasible Path

I knew I needed to find something else. My next thought was that I wanted to create an **enjoyable game**. With those two initial thoughts in mind, a third idea came shortly after: I needed to make a game with an **engaging loop** that was feasible to develop within my limited constraints. I wanted something that didn’t rely heavily on visuals but instead focused on **game design and replayability**.

This led me to the concept of a **procedural dungeon with rooms**. Why?
- The action happens inside the dungeon, so no need for vast, visually stunning environments like mountains or mystical forests.
- Procedural generation means replayability—a new dungeon every run, creating an **infinite replayable experience**.

### Inspirations

I started thinking about games I’ve played that use similar ideas. Two games stood out to me:
1. **God of War: Ragnarok - Valhalla DLC**
2. **Returnal**

Both are AAA games, but their **design philosophies** inspired me deeply. Let’s talk more about **God of War: Ragnarok - Valhalla DLC**, as it was the main influence.

### What Valhalla DLC Does Well

- **Roguelike Mechanics:**
  - You enter a level that is **randomly generated**, featuring temporary upgrades that enhance your performance. These upgrades **don’t carry over** to the next level, but certain currencies do, enabling **permanent upgrades**.
  - This balance of temporary boosts and long-term progression makes each run feel meaningful.

- **Story Integration:**
  - Even though it’s a roguelike, it intertwines story elements beautifully. Each run feels like a step toward something greater, keeping players invested in the **narrative** while enjoying the core gameplay.

- **Replayability:**
  - It has a **starting point** and an **end point**, but after reaching the end, the game’s core mechanics still offer infinite replayability.

### Defining My Project Goals

With these inspirations and ideas in mind, I knew exactly what I wanted from my project:
1. **A procedural dungeon crawler** for replayability.
2. **An engaging gameplay loop** with upgrades and progression mechanics.
3. **A subtle, cryptic story** that unfolds through gameplay but doesn’t overshadow the core mechanics.
4. **Infinite replayability**, even after finishing the main story.

### Supporting Documents

For more details and related documents, refer to the [The Starting Point Folder](./Documentation/The%20Starting%20Point/) in the repository. It contains:

1. **Document in Romanian (Raw):** [Initial Design Notes and Ideas](./Documentation/The%20Starting%20Point/code_name_abyss.docx)
2. **Document in English (Translated):** [Initial Design Notes and Ideas](./Documentation/The%20Starting%20Point/code_name_abyss.ro.en.docx)

With this foundation, I was ready to move forward. Let’s explore how these ideas shaped *Abyssborne* in the next chapter!

# **The Actual Start**

So, now with a well-enough planned plan, it was time to start the actual project. *(I say "well enough" because you can’t have everything planned out from the start. Things change along the way. Yes, a vision, a principal plan, can exist from the beginning, but some things evolve across the road—new ideas emerge, etc. If someone tells you they made a plan from the beginning, had everything paved from start to finish, and nothing changed, they’re lying to you.)*

### Beginning the Journey

As I had no prior experience with UE5, I needed to search the internet for resources and understand how Blueprints work. While it wasn’t overly difficult for me, thanks to my programming background and familiarity with many programming concepts, I understand that for others, it could be more challenging.

My first stop was **YouTube**, where I searched, "how to make a procedural dungeon generation in UE5." That’s when I stumbled upon a gem hidden in the dust. I found this guy: [REE-Animation](https://www.youtube.com/@REE-Animation), who had a playlist that was exactly what I needed: ["How To Create Epic Procedural Dungeons In Unreal Engine 5"](https://www.youtube.com/playlist?list=PLrZV1-GZa3Ds1-ON_oeWIdLHXCJ1QZH1P).

I can’t express how happy I was to discover this 5-video series. The tutorial was very well-made, and I learned so much for the journey ahead. I want to give a massive shoutout to **REE-Animation** and this great tutorial, which served as a huge starting point for my project. My motivation skyrocketed knowing I had such excellent help tailored precisely to what I needed.

### Utilizing Online Resources

The internet is vast and filled with resources. While I prefer watching **YouTube tutorials**, throughout this project, I explored:
- The official UE5 documentation
- Epic Games/UE5 forums
- Reddit
- StackOverflow
- Various articles and blog posts

There are resources for almost anything online (okay, not literally everything, but for the most part). With persistence, you can learn so much. This knowledge doesn’t just solve immediate problems but also helps you figure out new ones and come up with creative solutions later. You also gain new ideas as you internalize the concepts you’ve learned.

### Adapting the Tutorial

I created a new project and followed REE-Animation’s tutorial while putting my own fingerprint on it. I adapted and changed things to suit my preferences and, from time to time, sought other tutorials for specific aspects I wanted. I didn’t follow the tutorial step-by-step like a bot.

What makes this tutorial so brilliant is that it teaches key concepts while leaving gaps for you to fill in on your own. For example:
- **Elevator Room:** The tutorial creates a room for an elevator but doesn’t implement a working elevator, encouraging you to seek other tutorials.
- **AI System:** The tutorial builds a basic roaming AI that can follow the player but doesn’t implement damage or a full combat system, again prompting you to explore other resources.

These gaps allow you to take ownership of your project, which is essential for learning and creativity.

### Final Thoughts

Through this tutorial and the journey that followed, I learned that **everything is possible**. If you’ve made it this far in this documentation, know that you, too, can achieve whatever you put your mind to. This was my real starting point, and it paved the way for everything that followed.

Next, we’ll dive deeper into the **procedural dungeon system** and how it works.


---
---
---
FOR LATER
# **Game Description**

*Abyssborne* is a dark fantasy roguelite that thrusts players into shadowed, ever-changing dungeons filled with enemies, upgrades, and cryptic mysteries. As an Abyssborne vessel, reshaped by a higher being known as **The Weaver**, your purpose is shrouded in mystery. The game combines strategic combat, exploration, and a rich, hidden lore revealed through collectible letters.

---

# **Installation Guide**

### **For Players**

1. **Download the Game**
   - Visit the download link: [Download Abyssborne](https://drive.google.com/drive/folders/1hOFzNEi8PWO3oH_PJrmcNG5_5calXUdo?usp=sharing).

2. **Extract the Game**
   - Once downloaded, extract the `.zip` file to a folder of your choice.

3. **Run the Game**
   - Navigate to the extracted folder and double-click `Abyssborne.exe` to start playing.

> **Note:** Currently, the game is only available for **Windows** and has been optimized for this platform.

### **For Developers**

1. **Clone the Repository**
   - Use the following command to clone the repository:
     ```bash
     git clone https://alexandru-codarcea@dev.azure.com/alexandru-codarcea/JocUnreal/_git/JocUnreal
     ```

2. **Open with Unreal Engine**
   - Ensure you have **Unreal Engine 5.4.4** installed.
   - Open the `Abyssborne.uproject` file using Unreal Engine.

3. **Build and Play**
   - Build the project and launch it within Unreal Engine to test or modify the game.

---


