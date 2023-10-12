
# Table of Contents

1.  [Pre-Development Agenda](#org734a6dc)
    1.  [Books](#orge420df3)
    2.  [Activities](#orgcf99104)
        1.  [Game building](#orgc18e7a7)
        2.  [Research](#orgfa52824)
2.  [Development (tentative)](#org4a11ffc)

Thrive
A game engine focused on small teams and procedural generation


<a id="org734a6dc"></a>

# Pre-Development Agenda


<a id="orge420df3"></a>

## Books

1.  <span class="underline">Command Line Rust</span> to get started learning the language.
2.  <span class="underline">Foundations of Game Engine Development</span>, vols I and II. Learn the underlying math! This one requires the most attention.
3.  <span class="underline">Game Programming Patterns</span>, found at <https://gameprogrammingpatterns.com/>. This is just to be read, not worked out. If I want to use a pattern later, I can use this thing called a search engine and write &ldquo;<name of pattern> Rust&rdquo;.

Only the first one need be completely finished before starting development. The others can be a read-as-we-go deal.


<a id="orgcf99104"></a>

## Activities


<a id="orgc18e7a7"></a>

### Game building

Build a basic 3D game (by following a tutorial) in Unity, Unreal 4, or both. The goal is to get familiar with the features and what it feels like to build a game in each. A few hours in each should suffice for the beginning, but *should be a recurring step*, regularly returning to see what&rsquo;s available on the &ldquo;top level&rdquo; of oter engines.


<a id="orgfa52824"></a>

### Research

Consume many videos and podcasts on general game engine development. Always be listening to them. *This should primarily be high-level material*, focused on things like architecture and processes rather than the niceties of code.


<a id="org4a11ffc"></a>

# Development (tentative)

1.  Bootstrap. This means **basic systems**, including, but not limited to:
    1.  File I/O
    2.  Logging
2.  **Networking layer** for multiplayer. This means set up the client and server, and at least get some text packets going in TCP.
3.  **Graphics API**. Pick a graphics library, such as OpenGL or Vulcan or whatever, and figure out how we&rsquo;re gonna initialize/interact with it. Try to set up the abstraction so that we can change our minds later if we want, if that&rsquo;s feasible.
4.  **Asset pipeline**, at a high level. Just determine how we&rsquo;re gonna import assets and get the interface in place.
5.  **UI**, meaning UI for the game designer. This happens at such an early stage because we need to be able to dick with the engine from the developer perspective during developing.
6.  **World and scene graph**. A scene graph, or world graph, is just a DAG that puts objects in a hierarchy. If I move my arm, then my hand must move, too. We could represent this in our scene graph by making the hand node a child of the arm node. Simple.
7.  **Client state** for client and server. Suppose an object moves around in the server and all the clients need to see it. The plumbing in the networking layer to enable that must be built at this stage.
8.  **Physics**. Pick a physics engine or write one. Probably pick one, at least to begin. Figure out how to treat physics over the network. Think: how would two people play a ping-pong game over this network? How would the physics work?
9.  **Tools**. All the level editors, asset importers, whatever else. The mantra at this stage will have to be &ldquo;I am the only person who actually likes the terminal&rdquo;, because game devs want pointy-clicky tools.

