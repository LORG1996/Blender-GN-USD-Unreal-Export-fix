# 🛠️ Blender USD Surgical Fixer for UE5

<p align="center">
  
<img width="688" height="384" alt="Gemini_Generated_Image_jjgeyijjgeyijjge" src="https://github.com/user-attachments/assets/e8e067da-1965-4a62-9549-f97301a95cf0" />
</p>

This Blender add-on fixes common issues when exporting **Geometry Nodes (Instance on Points)** to **Unreal Engine 5** via USD. It ensures that instances are recognized as meshes and that materials are applied correctly.

## ✨ Features

*   **Instance Validation**: Automatically changes `None` type prototypes to `Mesh` so Unreal Engine can render them.
*   **Hierarchy Repair**: Renames internal meshes (adds `_geo` suffix) to prevent USD naming conflicts where a child has the same name as its parent.
*   **Material Binding Clean-up**: Strips local path prefixes from `material:binding`, making material links global (e.g., `/_materials/MyMaterial`).

## 📦 Installation

1.  Download the `usd_ue5_fixer.py` file from this repository.
2.  In Blender, go to **Edit > Preferences > Add-ons**.
3.  Click **Install...** and select the `.py` file.
4.  Enable the add-on: **Import-Export: USD UE5 Surgical Fixer**.

## 🚀 Workflow

1.  **Export from Blender**: Export your scene to USD. 
    > **Note**: Ensure that **"Instancing"** is enabled in the Blender USD export settings.
2.  **Run the Fixer**:
    *   Open the Sidebar in the 3D Viewport (press `N`).
    *   Navigate to the **USD Fixer** tab.
    *   Click the **Select & Fix USD** button and choose your exported file.
3.  **Import to UE5**: A new file with the suffix `_FIXED_FINAL.usd` will be created. Use this file to import into Unreal Engine via the **USD Stage Actor**.

---
*Developed by Vova. Optimized for architectural visualization and complex environment workflows.*
