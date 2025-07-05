---
layout: post
title: "Building an AI-Powered Travel Planner: My SheCodes Python AI Workshop Finale!"
date: 2025-07-05
categories: [Python, AI]
tags: [Python, AI, SheCodes, Travel, APIs]
---

# Building an AI-Powered Travel Planner: My SheCodes Python AI Workshop Finale! 🤖✈️

Hello, fellow coding enthusiasts! 👋 I’m thrilled to wrap up the **SheCodes Python AI workshop** and share my final project: an **AI-Powered Travel Planner**! This adventure taught me to weave together AI prompt engineering, live API data, JSON parsing, and vibrant Markdown styling. Let’s dive into the magic of building a dynamic, user-friendly app—and inspire you to create your own! 🚀🐍

## My Coding Journey So Far

If you’re new here, I’m Stephie Oj, a Business Analyst turned coding newbie, passionate about making tech fun and approachable. Through SheCodes, I’ve tackled HTML, CSS, JavaScript, Python basics, and now AI. This workshop was a game-changer, blending real-world data with AI creativity. Every bug I squashed felt like a mini victory—let’s celebrate these wins together! 🎉

## Final Project: AI Travel Planner 🌍

My capstone project is a console app that crafts personalized AI generated travel itineraries. Here’s what it does:
- Greets users with a colorful `rich.print()` banner
- Asks for **origin**, **destination**, and **trip duration**
- Fetches live weather data for both cities using the SheCodes Weather API
- Generates a tailored itinerary with the SheCodes AI API, sprinkled with emojis
- Displays the plan in styled Markdown using the `rich` library
- Wraps up with a heartfelt credit sign-off

Blending **weather data**, **AI responses**, **JSON parsing**, and **Markdown styling** was such a cool way to tie all my skills together! Check it out --> [Here](https://colab.research.google.com/drive/1KPh61zeTJ3FxGgvrD14iqVifioJMb77U?usp=sharing)😄

## What I Learned: Key Techniques & Takeaways

### ✔️ Mastering AI APIs for Smart Responses  
I crafted precise prompts to guide the SheCodes AI API to create concise, emoji-packed itineraries with transport, attractions, meals, and tips.

```python
prompt = (
    f"Create a {duration}-day travel itinerary from {origin} to {destination}. "
    "Include transport, attractions, meals, accommodations, and time-saving tips. "
    "Keep it under 15 lines, left-aligned, with a few emojis."
)
context = "You are an expert travel planner with deep knowledge of culture and logistics."
```

**Key Takeaway**: Clear prompts unlock AI’s potential—tweak tone and constraints to get polished, creative outputs! 🤖

### ✔️ Optimizing Prompts for Better Results  
Slightly sidetracked… iterating on prompts (e.g., adding “left-aligned” or “under 15 lines”) made my itineraries scannable and user-friendly. Seeing the AI respond to my tweaks was so rewarding! 😎

### ✔️ Fetching Live Data with Weather APIs  
I used the `requests` library to pull real-time weather data, parsing nested JSON to extract key details like temperature and conditions.

```python
res = requests.get(
    f"https://api.shecodes.io/weather/v1/current?query={location}&key={api_key}&units=metric"
).json()
temp = round(res["temperature"]["current"])
cond = res["condition"]["description"]
```

**Key Takeaway**: APIs bring apps to life! Practicing JSON parsing helped me grab exactly the data I needed. 🔍

### ✔️ Styling Outputs with the `rich` Library  
The `rich` library turned my AI-generated Markdown into vibrant, scannable console output.

```python
from rich.markdown import Markdown
itinerary = Markdown(response_data["answer"])
console.print(itinerary)
```

**Key Takeaway**: `rich` makes console apps pop—no GUI needed! It’s a fun way to elevate user experience. 🎨

### ✔️ Parsing JSON Like a Pro  
Navigating nested JSON from both weather and AI APIs became second nature, pulling out key data with ease.

```python
response_data = response.json()
answer = response_data["answer"]
```

**Key Takeaway**: JSON parsing is like solving a puzzle—master it, and API-driven projects become a breeze! 🧩

### ✔️ Crafting a Seamless User Experience  
I tied everything together with a welcoming banner, clear input prompts, and a warm sign-off, creating a smooth flow for users.

```python
def welcome():
    console.print("[purple bold]Welcome to the AI Travel Planner[/purple bold] 🤖🌍✈️")

def credit():
    console.print("\nThank you for planning your trip with [purple bold]Stephie Oj[/purple bold] 💕 Safe travels! ✈️")
```

**Key Takeaway**: A thoughtful UX, even in the terminal, keeps users engaged and makes your app feel polished! 💖

## Tips for Aspiring Coders 🧐
- **Start Simple**: Play with a basic API (like weather) before diving into AI.
- **Tweak Prompts**: Experiment with wording and constraints to shape AI outputs.
- **Use `rich`**: Add color and Markdown to make your console apps shine.
- **Practice JSON**: Write small scripts to navigate nested data—it’s a core skill!
- **Celebrate Wins**: Every bug fixed or feature added is a milestone—cheer yourself on! 🎉

## What’s Next for Me?  
I’m pumped to enhance my Travel Planner with error handling, caching, and maybe a web front-end. I’ll share the code on GitHub with a killer README to invite collabs. AI and Python are my new superpowers, and I’m ready to keep building cool things! 🚀

Let’s keep coding, creating, and exploring new possibilities together!  

Happy coding! Stephie Oj. 🐙💖