# Reddit-User-Persona-Generator

# Reddit User Persona Generator

This script analyzes a Reddit user's activity to generate a detailed user persona with citations, following a structured format without using OpenAI APIs.

## Features
- Scrapes user comments and posts via Reddit API
- Analyzes content using NLP techniques (NLTK, TextBlob)
- Generates comprehensive user persona with:
  - Personal details
  - Motivations
  - Personality traits
  - Behavior patterns
  - Goals and frustrations
- Includes direct citations for all persona elements
- Outputs results in markdown format

## Setup Instructions

### 1. Install Requirements

pip install praw nltk textblob python-dotenv


## 2. Create Reddit App
Go to https://www.reddit.com/prefs/apps

Click "Create App"

Select "script" type

Note your:

Client ID (under app name)

Client secret

## 3. Configure Environment
Create .env file with your credentials:

env
REDDIT_CLIENT_ID='your_client_id'
REDDIT_CLIENT_SECRET='your_client_secret'
REDDIT_USER_AGENT='persona_scraper/1.0 by your_username'
Usage
Run the script with:

bash
python reddit_persona.py
When prompted, enter a Reddit profile URL:

text
Enter Reddit profile URL: https://www.reddit.com/user/ExampleUser/

Output
The script generates a [username]_persona.txt file containing:

Structured persona with tables and bullet points

Direct citations linking to source content

Analysis of:

Personal details (location, occupation)

Motivations and frustrations

Personality traits

Behavioral patterns

## Sample Output Structure
**John Doe**

| PERSONAL DETAILS      |               |
|-----------------------|---------------|
| Location              | New York      |
| Occupation            | Developer     |

**MOTIVATIONS**
- Learning new technologies [Source]

**PERSONALITY**
| Outlook               | Positive      |

**BEHAVIOUR & HABITS**
- Frequently discusses programming [Source]

**FRUSTRATIONS**
- Difficulty finding documentation [Source]

"I love open source projects!" [Source]
## Notes
Respects Reddit API rate limits

Processes most recent 150 items (comments + posts)

Analysis based on linguistic patterns and statistical NLP

Persona details extracted through keyword matching and sentiment analysis
