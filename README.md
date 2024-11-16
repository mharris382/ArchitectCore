# ArchitectCore
# ArchitectCore

# Directory Structure



# Slot Masks
| Slot Name | Bit Index | Number |  Exclusive Slots | 
|-----------|-----------|--------|--------------------------|
| Wall      | 1         | 1      | Floor, Ceiling           |
| Door      | 2         | 2      | Window                   |
| Window      | 3         | 4      | Door                   |
| Corner Out    | 4         | 8      | Corner In            |
| Corner In    | 5         | 16      | Corner Out           |
| Floor    | 6         | 32      | Wall, Ceiling            |
| Ceiling    | 7         | 64      | Wall, Ceiling          |




# Assembly Tags



# Building Slots
The concept of a Building Slot is to match a generalized idea, like a door, floor or wall.  There are a number of slots that which can define a particular asset as well as spawning behavior.  
Windows and Doors work with the Building Cutter tool.  When the tool is set to Window Mode or Door Mode, it will mark overlapping walls (floors are planned) as a door or window(respectively).  These grid cells will then be spawned with the window recipe or the door recipe.   

[Insert Screenshot of Editor]


Note:  Doors or Windows can be ignored by the BuildingSpline Actor

Slots for Corners and Inverted Corners also define an additional spawning behavior which specifies how they relate to the adjacent walls (floors are planned).  
[Modes Table here]

## Spawning Modes

### Mesh Only
[Description Here]
### Assembly Only
[Description Here]
It is worth noting that the assembly can access the mesh pipeline and mesh material with tags.  
#### Built-In Tags
[Add Table for tags here]
### Combined
[Description Here]


# Building Spline
located in Content > Blueprints folder.  

## All Settings 
### 00 - Core
### 01 - Wall
### 02 - Floors (may need to make clear that ceiling is a floor)
