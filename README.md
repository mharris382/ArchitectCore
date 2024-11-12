# ArchitectCore
# ArchitectCore

# Directory Structure
ArchitectCore/
├── Content/
│   ├── Blueprints/                # Blueprint Building Spline and Building Cutter Actors
│   │   ├── Components/            # (Experimental planned with 5.5) Modular building modifiers using components
│   │   ├── Experimental/          # experiments
│   ├── Bonus/                     # Just a triplanar material that I find useful
│   ├── Core/                      # All the internal pcg systems that are core to the plugin
│   │   ├── ArchitectAssets/       # data asset definition for recipe sets used by PCG, The primary data asset class.  A full recipe would define each possible building slot
│   │   ├── ArchitectPipeline/     # data asset defintion to optionally override some or all parts of the spawning pipeline, can also use to 
│   │   ├── Graphs/                # PCG Graphs (see graph naming conventions)
│   │   │   ├── Defaults/          # Defualt Behaivors that can be overrides (see override graph section)
│   │   │   │   ├── Overrides/     # Override Behaviors that added to the pcg building pipeline
│   ├── Recipes/                   # Recipe Data
│   │   ├── Recipes/               #  Recipe Examples
│   │   ├── Pipeline/              #  Pipeline Examples
│   ├── Templates/                 # Blueprint Building Spline and Building Cutter Actors
│   │   ├── Assemblies/            # Packed Level Actors and PCG Data Assets
│   │   ├── Meshes/                # Template Building Meshes (used as defaults)
│   │   ├── Materials/             # Template Building materials (used as defaults)
│   ├── Presets/                   # Preset assets for PCG recipes, settings
│   └── UI/                        # User interface assets, like icons and widgets
├── Resources/                     # Non-Unreal assets (e.g., documentation, UI icons)
└── Source/                        # Plugin source code
    └── ArchitectCore/             # Main module. mostly constains custom editor structs QoL improvments




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
