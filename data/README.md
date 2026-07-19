# Data Directory

Due to file size constraints (GitHub's 100MB limit) and best practices for version control, the raw MIDI files are **not** stored in this repository. 

### How Data is Ingested
The dataset is hosted externally on a shared Google Drive:
🔗 **[Google Drive Dataset Link - midi-classic-music.zip](https://drive.google.com/file/d/1QJPbVi6q2QPIiD47ZBf9tDxhM4ON-7mj/view?usp=share_link)**

Our main Notebook uses the `gdown` Python library to automatically download the `.zip` file from this link into the temporary storage of the active compute cluster (Google Colab or Databricks) and extracts it into this `/data/` path at runtime.

**If you are running this project entirely offline (locally):**
1. Download the `midi-classic-music.zip` file manually from the [Google Drive link](https://drive.google.com/file/d/1QJPbVi6q2QPIiD47ZBf9tDxhM4ON-7mj/view?usp=share_link).
2. Place the downloaded `.zip` file directly into this `data/` folder.
3. Skip the `gdown` download script (Cell 2) in the notebook and proceed directly to the file extraction step.
