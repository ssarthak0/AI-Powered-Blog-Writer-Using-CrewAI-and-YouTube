# 🤖 AI-Powered Blog Writer Using CrewAI and YouTube

This project utilizes [CrewAI](https://github.com/joaomoura/crewai) to automate the process of researching and writing blog posts based on YouTube videos. It orchestrates two AI agents: a blog researcher and a blog writer, to collaboratively generate insightful blog content.

## 📂 Project Structure

- `crew.py`: Initializes and runs the CrewAI agents and tasks.
- `agents.py`: Defines the blog researcher and writer agents.
- `tasks.py`: Specifies the research and writing tasks assigned to the agents.
- `tools.py`: Implements the YouTube channel search tool.
- `requirements.txt`: Lists all necessary Python dependencies.

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/ssarthak0/AI-Powered-Blog-Writer-Using-CrewAI-and-YouTube
cd AI-Powered-Blog-Writer-Using-CrewAI-and-YouTube
```

### 2. Set Up a Virtual Environment

```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory and add your OpenAI API key:

```env
OPENAI_API_KEY=your_openai_api_key
```

### 5. Run the Application

```bash
python crew.py
```

## 🧠 Agents Overview

### Blog Researcher

- **Role**: Blog Researcher from YouTube Videos
- **Goal**: Retrieve relevant video transcriptions for the specified topic from the provided YouTube channel.
- **Backstory**: Expert in understanding videos in AI, Data Science, Machine Learning, and Generative AI, providing insightful suggestions.
- **Tools**: Utilizes a YouTube channel search tool to find pertinent videos.

### Blog Writer

- **Role**: Blog Writer
- **Goal**: Craft compelling tech stories based on the researched YouTube video content.
- **Backstory**: Skilled in simplifying complex topics and creating engaging narratives that educate and captivate readers.
- **Tools**: Leverages the same YouTube channel search tool to access video content.

## 📝 Tasks Breakdown

### Research Task

- **Description**: Identify and gather detailed information about the specified topic from the YouTube channel's videos.
- **Expected Output**: A comprehensive 3-paragraph report based on the video's content related to the topic.
- **Assigned Agent**: Blog Researcher

### Writing Task

- **Description**: Summarize the information obtained from the YouTube channel on the specified topic and create blog content.
- **Expected Output**: A well-structured blog post summarizing the video's content on the topic.
- **Assigned Agent**: Blog Writer
- **Output File**: `new-blog-post.md`

## 🔧 Tools Utilized

### YouTube Channel Search Tool

- **Purpose**: Searches for videos within a specific YouTube channel based on the provided topic.
- **Configuration**: Initialized with the YouTube channel handle `@krishnaik06`.

## 📄 Output

Upon execution, the application will generate a markdown file named `new-blog-post.md` containing the blog post derived from the YouTube video's content on the specified topic.

## 📌 Notes

- Ensure that the YouTube channel handle provided in the `YoutubeChannelSearchTool` is correct and accessible.
- The application currently targets the `@krishnaik06` YouTube channel. Modify the handle in `tools.py` if you wish to target a different channel.
- The quality of the generated blog post heavily depends on the relevance and quality of the YouTube videos retrieved.

## 📚 References

- [CrewAI Documentation](https://docs.crewai.com/)
- [LangChain Documentation](https://docs.langchain.com/)
- [OpenAI API](https://openai.com/api/)
- [YouTube Data API](https://developers.google.com/youtube/v3)

## 🛠️ Future Enhancements

- Integrate additional data sources beyond YouTube for more comprehensive research.
- Implement a GUI using Streamlit for user-friendly interactions.
- Add functionality to schedule regular blog post generations on trending topics.

---
