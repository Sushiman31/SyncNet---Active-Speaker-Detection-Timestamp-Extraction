## 🗣️ **SyncNet - Active Speaker Detection & Timestamp Extraction**  

This project is a **modified version of SyncNet**, where the `run_visualise.py` script has been enhanced to **detect active speakers**, **display real-time visualization**, and **record their activity timestamps** in a JSON file.  

These timestamps can be used to **extract speakers** in **dyadic databases**.

---

## ✨ **Modifications & Features**  

🔹 **Enhancements to `run_visualise.py`**:  
- **Detects the active speaker** based on lip movement and audio synchronization.  
- **Displays real-time visualization** of detected speakers directly on the video.  
- **Records speaker activity timestamps** (`start`, `end`, `position`) in a JSON file.  
- **Determines the speaker's position** (`left` or `right`).  

🔹 **New Output Files**:  
- A **`speaking_intervals.json`** file is generated, containing **timestamps for each speaker**.  
- A **video with bounding boxes** around detected speakers is saved for **real-time visualization**.  

---

## 📂 **Example JSON Output**  

If two speakers are talking:
```json
{
    "0": [
        {
            "start": 2.0,
            "end": 4.5,
            "position": "left"
        },
        {
            "start": 6.0,
            "end": 9.2,
            "position": "left"
        }
    ],
    "1": [
        {
            "start": 3.5,
            "end": 5.1,
            "position": "right"
        },
        {
            "start": 10.0,
            "end": 12.8,
            "position": "right"
        }
    ]
}
```

---

## 🚀 **How to Use This Repository?**  

⚡ **1️⃣ Install SyncNet**  
Follow the installation instructions from the **official SyncNet GitHub**:  
🔗 [SyncNet GitHub](https://github.com/joonson/syncnet_python)

⚡ **2️⃣ Run Our Modified Version**  
Use `run_visualise_.py` instead of `run_visualise.py`:
```bash
python run_visualise_.py --videofile /path/to/video.mp4 --reference name_of_video
```

⚡ **3️⃣ Retrieve the Generated Timestamps & Video**  
- The detected timestamps are saved in **`speaking_intervals.json`**, which can be used for:  
  ✅ **Segmenting audio by speaker**  
  ✅ **Building dyadic databases**  
  ✅ **Analyzing turn-taking in conversations**  
- The **processed video** shows detected speakers in real time, with **bounding boxes** indicating who is speaking.

---

## 🎯 **Why Use This Modification?**  
✅ **Facilitates speaker extraction** for dyadic datasets.  
✅ **Automates timestamp annotation** for each speaker.  
✅ **Adds speaker position detection** (`left` or `right`).  
✅ **Provides real-time visualization** of active speakers in the video.  

---

## 🛠️ **Credits**  
This project is based on **SyncNet**, developed by [joonson](https://github.com/joonson/syncnet_python).  
Modifications were made to **extract active speakers, provide real-time visualization, and generate speaker timestamps**.  
