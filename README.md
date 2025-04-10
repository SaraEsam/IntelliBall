🛠️ Installation
✅ Option 1: For notebooks (like Colab or Jupyter)
At the top of your notebook, add:

!pip install ultralytics deep_sort_realtime filterpy torch torchvision gradio

✅ Option 2: For local setup
Create a requirements.txt with the following content:

ultralytics
deep_sort_realtime
filterpy
torch
torchvision
gradio
opencv-python
numpy
Then install everything with:

pip install -r requirements.txt

🚀 How to Run
1. Clone the repository

git clone https://github.com/yourusername/offside-detector.git
cd offside-detector
2. Run the application

python app.py
This will launch a Gradio interface in your browser.


📸 How It Works
Object Detection: Each frame is analyzed using YOLOv8 to detect players (class 0) and the ball (class 32).

Tracking: Players are tracked across frames using Deep SORT.

Pass Detection: If the ball moves significantly, the system considers this a pass and freezes that frame.

Offside Rule Check:

Captures all player positions at the moment of the pass.

Identifies the two closest defenders to the goal.

Checks if the attacking player is ahead of the second last defender.

Annotation:

Draws a vertical line at the second last defender's position.

Adds a label (Offside or Not Offside) to the video.

🌍 Language Support
The interface and results are displayed in Arabic.

📥 Input Format
Supported video format: .mp4

Preferably use short clips with a clear view of players and ball.

🧪 Example Use
Upload a video like this:

A short clip showing a potential offside situation.

The ball must be visible clearly during the pass.

📤 Output
A processed video showing the offside decision.

Text output: ✅ Offside or ❌ Not Offside

📌 Notes
Accuracy depends on video clarity and player visibility.

Current model assumes a fixed camera angle and basic field view.

Can be improved with team detection or line marking.

🧠 Future Improvements
Team classification (to differentiate defenders from attackers).

Multiple camera support.

Real-time live feed support.

👨‍💻 Author
Developed by [Sara Esam] – feel free to fork, contribute, or get in touch!
