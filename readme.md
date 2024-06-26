
### Step 2: Install the Package in Blender

To install the package in Blender’s Python environment:

1. **Locate Blender’s Python Executable:**
   - Open Blender.
   - Go to the `Scripting` workspace.
   - Open a new Text Editor and run the following script to print Blender's Python executable path:
     ```python
     import sys
     print(sys.executable)
     ```

2. **Open a Terminal and Navigate to Blender’s Python Directory:**
   - Copy the path printed from the above script.
   - Open a terminal and navigate to Blender’s Python directory:
     ```bash
     cd /path/to/blender/installation
     ```

3. **Install the Package:**
   - Navigate to the directory containing `setup.py` and run:
     ```bash
     /path/to/blender/python/bin/python3.7m -m pip install .
     ```

### Step 3: Create a New Script in Blender to Use the Package

1. **Open Blender and Go to the Scripting Workspace:**
   - Open Blender.
   - Switch to the `Scripting` workspace.

2. **Create a New Script:**
   - Click `New` in the Text Editor panel to create a new script.
   - Save this script with a name, for example, `run_elbow_creator.py`.

3. **Write the Script to Use the Package:**

```python
import bpy
from elbow_Creator import create_elbow

# Example usage
radius = 1
point1 = (0, 0, 0)
point2 = (2, 2, 0)
create_elbow(radius, point1, point2)
