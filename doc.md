# Cutscenes

Each panel of a cutscene can specify the sprites and text to be displayed, and
music and voice clips to play. Each panel of a cutscene is created in code 
with the line `my_cutscenes_name = new Cutscene()`.

Adding a sprite to a cutscene can be done by using the `addSprite` method on it.
The parameters to this are:

`addSprite(spriteName, x, y, width, height)`

Text is added to the scene with:

`addLine(text, x, y, size, color)`

The `music` and `voice` properties specify a music clip and voice clip to be played
during the scene (if any).


### Example:
```
cut_intro1 = new Cutscene()
cut_intro1.music = "intro"
cut_intro1.voice = "intro_va_1"
cut_intro1.addSprite("house",0,0,400,200)
cut_intro1.addSprite("jeffry_down", 70, -48,32,50)
cut_intro1.addLine("I like this new neighborhood", 20, 20, 12, "white")
cut_intro1.addLine("I think I'll go say hi to my neighbor...", 20, 0, 12, "white")
```

This creates the cutscene `cut_intro1` (each cutscene panel needs it's own name), 
adds the name of a music and voice clips, and then adds two sprites and two lines 
of text. The fastest way to create a new cutscene panel is to copy this one, and 
change the names from `cut_intro1` to the name of the cutsene you're developing
(though probably without the music and voice lines) .

### New Cutscene Panels
Create new cutscene panels in the `cutscenes` file. During development, you will
want a fast way to view/load your cutscene panel while you're building it. 

To do this, start the project running, and then in the console panel type (or copy/paste)
the line into the bottom panel after the `>` character.

```
cutscene_manager.dev(cut_intro2)
```
where you replace `cut_intro1` with the name of the cutscene you're currently 
working on. This will restart the cutscene you named.

# Maps
Maps are started from the `set_map` function in the `maps` file. This function
is responsible for spawning entities for the given map, adding them to the 
entities collection, setting their location and starting the music for
that level. During development, the map can be changed immediately by running
the `set_map` function direction in the console. 

Example:
```
set_map("basement")
```



# dialog for end scene
```
haiku: Huh? who are you? and.. where am I..?

jeffery: uhh... werent you the monster?

haiku: Monster? Im 10!

jeffery: what do you mean??

haiku: wait...

Jeffery: what?

haiku: I think i remember now.... i think that doll...

jeffery: oh, you mean the doll with the red dress?

haiku: yes! Asuka.. that betrayed me.

jeffery: How?

Hakiu:When i lost my parents, the doll had just... appeared by me, i dont know how
or why, but she looked so pretty, so i thought i could trust her

jeffery: oh no

hakiu: So... i trusted her and i lost my memory- i think she..

jefery: Gave you a taco bell potion?

haiku: No... made me a monster?

jeffery: So no taco bell?

Haiku: No, no taco bell.

jeffery: oh... well where are you gonna go now?

haiku: i dont know...

jeffery: So.. do you need somehwere to live?

haiku; i suppose, i cant live here with that horrible doll..

jeffery: I guess you can come live with me?

haiku: I- really?

jeffery: Yeah, i guess sure


Haiku and jeffery lived as a happy family and moved away from the neighborhood,
```
**the end**

