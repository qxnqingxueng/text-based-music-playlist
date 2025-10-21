# 🎵 Text-Based Music Playlist Manager (C++)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vqIeWrpGGLgabIVm-zx5-CUPyVCXHT2c?usp=sharing)

---

## 1️⃣ Project Overview
The **Text-Based Music Playlist Manager** is a fully text-driven application developed in **C++**, designed for music enthusiasts to efficiently organize, browse, and manage their song collections through a console interface.  
The system is structured around **Object-Oriented Programming (OOP)** principles, ensuring code modularity, scalability, and clarity.

---

## 2️⃣ System Architecture and Implementation

### 🧩 Core Design
- **Data Structure:**  
  Implements a **Doubly Linked List**, where each node represents a single song and stores its attributes:
  - Song name  
  - Singer  
  - Duration (mm:ss)  
  - Genre  

- **Class Hierarchy:**  
  - `Playlist` — Base class defining the playlist structure and core methods.  
  - `SongPlaylist` — Derived class implementing the functional operations for managing songs.

- **Data Persistence:**  
  The program automatically reads song data from `song.txt` at startup and writes the updated, sorted playlist back to the same file upon exit.

---

## 3️⃣ Core Features and Menu Functions

The program provides an intuitive **10-option menu** for managing the playlist:

| Option | Functionality | Key Scenarios Handled |
|:------:|----------------|------------------------|
| 1 / 2 | **Next / Previous Song** | Navigate forward or backward. Handles end or beginning of playlist. |
| 3 | **Edit Current Song** | Modify details (name, length, singer, genre) of the current song. Includes input validation. |
| 4 | **Delete Current Song** | Remove the current song. Handles deletion until playlist becomes empty. |
| 5 | **Search Song** | Find a song by title and play it. Displays message if not found. |
| 6 | **Recommend by Genre** | Suggest songs from the same genre. Handles empty genre cases. |
| 7 | **Add Song** | Insert a new song with full validation and duplicate prevention. |
| 8 | **Display All Songs** | List all songs currently in the playlist. |
| 9 | **Shuffle Songs** | Randomize song order within the playlist. Handles empty playlists. |
| 10 | **Exit Program** | Confirm exit, sort songs, destruct playlist, and save to `song.txt`. |

---

## 4️⃣ Input and Requirement Validation

The system performs comprehensive validation checks to maintain data integrity:

1. **Input Range Check:**  
   Ensures numerical inputs (like menu options) fall within valid range (1–10).

2. **String Format Check:**  
   Validates song titles and artist names to ensure they’re not empty and begin with a capital letter or digit.

3. **Song Length Check:**  
   Enforces strict `mm:ss` formatting where minutes and seconds range from 00–59.

4. **Empty Playlist Handling:**  
   Displays warnings when operations like display or shuffle are attempted on an empty list.

---

## 5️⃣ How to Compile and Run

### 🧱 Required Files
- `playlist.h`  
- `songplaylist.h`  
- `songplaylist.cpp`  
- `main.cpp`  
- `song.txt` (data file)

### ⚙️ Compilation Steps
```bash
g++ *.cpp -o main.exe
./main.exe
