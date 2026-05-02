# Blender USD Surgical Fixer for UE5

<img width="688" height="384" alt="Gemini_Generated_Image_jjgeyijjgeyijjge" src="https://github.com/user-attachments/assets/e8e067da-1965-4a62-9549-f97301a95cf0" />

This Blender add-on fixes common issues when exporting **Geometry Nodes (Instance on Points)** to **Unreal Engine 5** via USD.

## Features

- **Instance Validation**: Fixes `None` type prototypes to `Mesh` for proper rendering in UE5.
- **Hierarchy Fix**: Renames internal meshes to avoid USD naming conflicts (Parent/Child identical name error).
- **Material Binding**: Cleans material paths by removing local prefixes, making bindings global (e.g., `/_materials/MyMaterial`).

## Installation
1. Download the [USD_Fix.zip](https://github.com/user-attachments/files/27309736/USD_Fix.zip).
2. In Blender, go to `Edit > Preferences > Add-ons`.
3. Click `Install` and select the downloaded `.zip` file.
4. Enable the add-on: **USD UE5 Surgical Fixer**.

## How to Use
1. Export your scene from Blender to USD (ensure "Instancing" is enabled).
2. Open the Sidebar in 3D Viewport (press `N`).
3. Find the **USD Fixer** tab.
4. Click **Select & Fix USD** and choose your exported file.
5. A new file with the suffix `_FIXED_FINAL` will be created in the same folder.
6. Import this fixed file into Unreal Engine.
