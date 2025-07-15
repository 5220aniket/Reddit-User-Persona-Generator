# Reddit-User-Persona-Generator

Generates comprehensive user personas from Reddit profiles using OpenAI's GPT-4. Analyzes comments/submissions to create structured personality profiles with verified sources.

## Features
- Scrapes Reddit user content (comments & submissions)
- Generates structured personas with:
  - Demographic info (Age, Occupation, Location)
  - Personality traits (MBTI dimensions)
  - Motivations, Goals, and Frustrations
  - Direct quotes with source links
- Saves output as Markdown-formatted text files

## Requirements
- Python 3.7+
- Reddit API credentials
- OpenAI API key (GPT-4 access)

## Setup
1. Install dependencies:

pip install praw openai==0.28


Add your API credentials in the notebook:

REDDIT_CLIENT_ID = 'your_client_id'
REDDIT_CLIENT_SECRET = 'your_client_secret'
REDDIT_USER_AGENT = 'your_user_agent'
OPENAI_API_KEY = 'your_openai_key'


## Usage
Run all notebook cells
Call the generator with a Reddit profile URL:
generate_persona_from_reddit("https://www.reddit.com/user/username/")
Output includes:

- Markdown-formatted persona in Jupyter
- Text file with sources (username_persona.txt)

## Output Structure

# [Name]
**AGE** | [Value]
**OCCUPATION** | [Value]
**STATUS** | [Value]
**LOCATION** | [Value]
**TIER** | [Value]
**ARCHETYPE** | [Value]

## [Trait Summary]

### MOTIVATIONS
- [Category]
  • [Sub-motivation]

### PERSONALITY
| [Trait] | [Trait] |
|---------|---------|
| [Value] | [Value] |

**BEHAVIOUR & HABITS**
- [Observation] [Source]

"Direct quote" [Source]

## Notes
Uses GPT-4 for persona generation (requires OpenAI access)

Processes the latest 150 activities (100 comments + 50 submissions)

Includes source verification for all claims

Handles private/deleted content gracefully



# Key highlights:
1. Requires valid Reddit app credentials and OpenAI API key
2. Specifically uses OpenAI v0.28 API (compatible with GPT-4)
3. Output follows a strict markdown template with source citations
4. Includes error handling for API limits and private profiles
5. Generates both in-notebook preview and text file output

# Remember to:
- Keep your API keys secure
- Check Reddit's API terms of service
- Verify OpenAI's GPT-4 usage policies
- Handle user data responsibly (PII considerations)

