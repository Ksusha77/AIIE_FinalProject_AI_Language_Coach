# AIIE_FinalProject_AI_Language_Coach

# AI Language Coach

Learning a new language can be tough. You need to practice talking, learn new words, get the pronunciation right, and it has to be fun so you don't give up. It’s also hard to find a practice partner who is always available and can help you with all of these things at once. Many apps focus on just one thing, like vocabulary flashcards or grammar drills, but rarely combine everything in an interactive way.

### The solution 
We created an "AI Language Coach" that you can run right from your code editor. It’s a simple, menu-based program that offers several ways to practice and learn:

* Practice Conversation: You can chat with the AI in the language you're learning. It will reply to you, translate what it said, and even explain key vocabulary words from its response.
* Create Visual Flashcards: If you have a list of words you want to learn, the tool will generate digital flashcards for you. Each card shows the word, its translation, and a custom image that helps you remember it.
* Hear Pronunciation: You can type in any word or phrase, and the AI will generate audio of how it's pronounced in the language you're studying.
* Play a Vocabulary Game: For a fun challenge, you can ask the AI to create a simple matching game based on a topic of your choice (like food or travel).

## Screenshots of the Solution

Here's a peek at what the AI Language Coach looks like in action.

<img width="670" alt="Screenshot 2025-06-13 at 11 15 59 AM" src="https://github.com/user-attachments/assets/29ce3f11-27b0-4d7a-9763-8471a154013a" />


Caption: The main menu lets you choose what you want to do.

<img width="687" alt="Screenshot 2025-06-13 at 11 16 46 AM" src="https://github.com/user-attachments/assets/db076b4e-8449-412b-bb9d-4e32cac609c1" />


Caption: Practicing a conversation in Spanish, with instant translations and vocabulary help.

<img width="1054" alt="Screenshot 2025-06-13 at 11 22 58 AM" src="https://github.com/user-attachments/assets/e41faab4-051f-4892-8083-22105053ee3f" />


Caption: A visual flashcard for the word "cat" in Japanese, with an AI-generated image.

## Technologies, Models, and APIs Used

* Python: The entire application is written in Python. It's a great language for building tools like this because it's easy to read and has a lot of helpful libraries.

* Google's Gemini Models: This is the brain of our application. We used several different Gemini models for their special abilities:
  * Gemini 1.5 Flash (gemini-1.5-flash): We used this model for all the text-based tasks. It's super fast and smart, which is perfect for having a real-time conversation, translating text, and creating the vocabulary games.
  * Gemini Text-to-Speech (gemini-2.5-flash-preview-tts): To help with pronunciation, we used this model to turn text into spoken audio. It gives a very natural-sounding voice.
  * Gemini Image Generation (gemini-2.0-flash-preview-image-generation): This model creates the images for our visual flashcards. We tell it what to draw, and it creates a simple, colorful picture for us.

* How We Used Multimodality: Multimodality just means using different types of information at once (like text, audio, and images). Our project is a great example of this! We take a word (text), generate a picture for it (image), and can even say it out loud (audio). This creates a much richer and more effective learning experience than just using text alone.
* Python Libraries:
  * google-generativeai: The official Google library to connect our code to the Gemini models.
  * IPython: Used to display the images and play the audio directly in our programming environment (like Google Colab).
  * Pillow (PIL) and wave: These are helper libraries for handling the image and audio file data.
 
### Evaluating Our Results
We wanted to make sure the output from the AI was actually helpful and high-quality.
When we first tried to make image flashcards, we just asked the AI to "make a picture of 'cat'". But if the user was learning Spanish, the AI sometimes got confused and made a generic image.

Our fix: We improved this by creating a two-step process. First, we ask the text model to translate "cat" into Spanish ("gato"). Then, we feed that translated word, "gato," to the image model. This gave us much more accurate and relevant pictures for the flashcards. The code for this fix is clearly marked in the generate_flashcard_image function.

<img width="1138" alt="Screenshot 2025-06-13 at 11 11 07 AM" src="https://github.com/user-attachments/assets/2517c1d1-6927-49c7-b12c-93c3f83ea831" />


## Our experience 
Building the AI Language Coach was a fantastic experience. It was exciting to see how we could connect different AI models to build a single, useful application. The biggest takeaway was learning how to think like an engineer—identifying a problem, breaking it down, and using the right tools to build a solution. We learned how to write better prompts to get what we wanted from the AI and how to handle unexpected errors. This project showed us that with modern AI, a small amount of code can go a long way in creating something powerful and fun to use.
