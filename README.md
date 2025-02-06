# Auto-Yuto

This project automates the creation of AI-generated videos using ChatGPT for text generation, DALL·E for images, and MoviePy for video editing. The output is a **silent video** with an AI-generated image and text overlay.

---

## **Tasks Breakdown**

### **1. Set Up the Environment**

- Install dependencies:
  ```bash
  pip install openai moviepy google-auth google-auth-oauthlib google-auth-httplib2 googleapiclient
  ```
- Set up API keys for **OpenAI** and **YouTube Data API**.
- Enable YouTube Data API v3 in Google Cloud Console.

### **2. Generate AI-Based Text Content**

- Select a random theme from a predefined list.
- Use ChatGPT to generate a short script.
- Save the text for later use.

### **3. Generate an AI Image Using DALL·E**

- Use the generated text to create an image prompt.
- Fetch the image and save it locally.

### **4. Create a Silent Video with Text Overlay**

- Use **MoviePy** to:
  - Load the AI-generated image.
  - Overlay the generated text.
  - Set the video duration (e.g., 10 seconds).
  - Export the final video as `final_video.mp4`.

### **5. Automate Video Upload to YouTube (Optional)**

- Use the YouTube Data API to upload videos.
- Provide a title, description, and tags.
- Ensure the video is set to public.

### **6. Automate the Entire Process**

- Schedule the script using **cron jobs** (Linux/macOS) or **Task Scheduler** (Windows).

Example cron job (runs every day at 6 PM):

```bash
0 18 * * * /usr/bin/python3 /path/to/your_script.py
```

---

## **Future Improvements**

- Add multiple images per video.
- Use AI-generated transitions.
- Integrate social media auto-posting.

---

## **Project Structure**

```
/ai-video-generator
├── scripts
│   ├── generate_text.py
│   ├── generate_image.py
│   ├── create_video.py
│   ├── upload_youtube.py
│   ├── main.py
├── assets
│   ├── images/
│   ├── videos/
│   ├── texts/
├── README.md
```

---



