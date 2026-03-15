# 🤖 AI Product Manager Crew with VisionTool

This project demonstrates how to build a collaborative team of AI agents using [CrewAI](https://github.com/joaomdmoura/crewai) to perform product analysis and planning from an image. This includes image understanding, design recommendations, and user story creation.

## 📌 Purpose

The goal is to simulate a **Product Management workflow** where different specialized AI agents perform specific tasks using a shared context, enabling the generation of user stories based on visual inputs.

## 🧠 Agents Involved

1. **Image Describer Agent**

   * Describes the visual content of an image accurately.
   * Uses `VisionTool()` for image processing.

2. **Designer Agent**

   * Analyzes the image description.
   * Suggests improvements or enhancements from a design perspective.

3. **Product Manager Agent**

   * Uses both the image description and design suggestions.
   * Creates and prioritizes user stories.

## 🛠️ Tools and Libraries

* Python 3 (Google Colab)
* [CrewAI](https://pypi.org/project/crewai/)
* [OpenAI GPT-4o](https://openai.com)
* `VisionTool` (CrewAI tools)
* Pillow (`PIL`) for image handling
* Google Colab `userdata` for managing API keys

## 📷 How it Works

1. Load an image from the working directory.
2. Initialize the AI agents with their roles, goals, and backstories.
3. Use CrewAI's `Crew()` and `Task()` classes to assign responsibilities and define execution order.
4. Each agent uses a shared context to enhance decision-making.
5. The final output consists of:

   * A detailed image description
   * Design recommendations
   * Three prioritized user stories

## 🧪 Example Image Used

Make sure `image1.png` is available in `/wherever/the/image/is/stored`.

## 💡 Usage

```python
!pip install 'crewai[tools]'
```

Make sure you have an OpenAI API key and optionally use:

```python
from google.colab import userdata
api_key = userdata.get('NotebookLM')
os.environ['OPENAI_API_KEY'] = api_key
```

## ✅ Output Sample

Once executed, you'll receive:

* ✔ A visual description
* ✔ Three improvement suggestions
* ✔ A prioritized list of user stories
