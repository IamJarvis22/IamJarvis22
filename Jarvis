- 👋 Hi, I’m @IamJarvis22
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
IamJarvis22/IamJarvis22 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import speech_recognition as sr
from gtts import gTTS
import os

# Initialize the recognizer
r = sr.Recognizer()

# Function to convert text to speech
def speak(text):
    tts = gTTS(text)
    tts.save("output.mp3")
    os.system("mpg321 output.mp3")

# Main function
def main():
    speak("Hello, I am your basic virtual assistant. How can I assist you today?")

    with sr.Microphone() as source:
        print("Listening...")
        audio = r.listen(source)

    try:
        text = r.recognize_google(audio)
        print("You said: " + text)
        speak("You said: " + text)
    except sr.UnknownValueError:
        print("I didn't catch that. Please repeat.")
        speak("I didn't catch that. Please repeat.")
    except sr.RequestError as e:
        print("Sorry, I'm experiencing some technical issues.")
        speak("Sorry, I'm experiencing some technical issues.")

if __name__ == "__main__":
   
