---
layout: page
title: PhD Apply Agent
description: Intelligent AI agent that automates PhD application outreach using Google Search API and custom email generation
img: assets/img/phd-agent.jpg
importance: 1
category: fun
github: https://github.com/aakash-priyadarshi/phd-apply-agent
---

An intelligent automation system that streamlines the PhD application process by researching professors, analyzing compatibility, and generating personalized outreach emails. This AI-powered agent leverages Google Search API and LLM capabilities to match applicants with potential PhD advisors at scale.

### Project Overview

Applying for PhD programs often involves reaching out to hundreds of professors across multiple universities. This project automates the time-consuming process of finding relevant professors, analyzing their research interests, and crafting personalized introduction emails—transforming weeks of manual work into an automated, intelligent workflow.

### Key Features

1. **Intelligent Professor Discovery**
   - Uses Google Search API to find professors based on research interests and field
   - Filters results by university, department, and research focus
   - Gathers professor information including email addresses, recent publications, and research areas

2. **Profile Matching & Compatibility Analysis**
   - Analyzes applicant's research interests against professor's work
   - Scores compatibility based on research overlap, publication topics, and expertise
   - Prioritizes potential advisors with the highest match scores

3. **AI-Powered Email Generation**
   - Generates highly personalized outreach emails for each professor
   - Incorporates specific research details, recent publications, and mutual interests
   - Maintains professional tone while showcasing genuine interest
   - Customizable templates for different scenarios (cold email, referral-based, etc.)

4. **Bulk Email Automation**
   - Sends personalized emails to multiple professors efficiently
   - Built-in rate limiting to avoid spam detection
   - Email tracking and response management
   - Follow-up scheduling capabilities

5. **Research Context Integration**
   - Pulls recent publications from Google Scholar
   - Analyzes professor's research group and lab focus
   - Identifies potential funding opportunities and open positions

### Technical Stack

- **AI/ML**: OpenAI GPT-4 for email generation and analysis
- **APIs**: Google Search API, Google Scholar integration
- **Backend**: Python, FastAPI
- **Email**: SMTP integration with Gmail API support
- **Data Processing**: BeautifulSoup for web scraping, Pandas for data management
- **Storage**: SQLite/PostgreSQL for tracking applications and responses

### Workflow Architecture

```
1. Input: User profile (research interests, background, target schools)
   ↓
2. Google Search API: Find relevant professors
   ↓
3. Data Collection: Gather professor details and publications
   ↓
4. AI Analysis: Match profile with professor interests
   ↓
5. Email Generation: Create personalized outreach emails
   ↓
6. Bulk Sending: Automated email dispatch with tracking
   ↓
7. Response Management: Track replies and schedule follow-ups
```

### Key Components

**Professor Search Module**
```python
# Search for professors by field and interests
professors = search_professors(
    research_area="machine learning",
    universities=["MIT", "Stanford", "CMU"],
    min_publications=10
)
```

**Compatibility Scoring**
- Semantic similarity between applicant and professor research interests
- Publication overlap analysis
- Recent activity and availability indicators

**Email Personalization**
- References specific papers by the professor
- Highlights relevant applicant achievements
- Proposes concrete research collaboration ideas
- Maintains authentic, non-generic tone

### Use Cases

- **PhD Applicants**: Automate outreach to potential advisors across multiple universities
- **Research Collaboration**: Find and contact professors for research partnerships
- **Postdoc Applications**: Adapt the system for postdoctoral position searches
- **Industry-Academia Connections**: Companies seeking academic collaborators

### Features & Capabilities

✅ **Smart Search**: Finds professors matching specific research criteria  
✅ **Profile Analysis**: Evaluates compatibility between applicant and advisor  
✅ **Custom Emails**: Generates unique, personalized messages for each professor  
✅ **Bulk Operations**: Sends hundreds of emails efficiently  
✅ **Response Tracking**: Monitors replies and manages follow-ups  
✅ **Anti-Spam Protection**: Built-in rate limiting and ethical sending practices  
✅ **Template Library**: Multiple email templates for different scenarios  

### Ethical Considerations

This tool is designed to facilitate genuine academic outreach, not spam:
- Encourages meaningful personalization based on actual research fit
- Includes rate limiting to prevent overwhelming professor inboxes
- Promotes quality over quantity in PhD applications
- Respects email best practices and anti-spam regulations

### Performance Metrics

- **Time Savings**: Reduces manual outreach time by 95% (from ~5-10 minutes per email to seconds)
- **Personalization Quality**: High relevance scores in generated emails
- **Response Rate**: Improved response rates compared to generic templates
- **Scalability**: Can process and contact 100+ professors in a single session

### Repository

- GitHub Repository: [PhD Apply Agent](https://github.com/aakash-priyadarshi/phd-apply-agent)

### Configuration

The system supports customizable parameters:
- Search filters (university ranking, research area, publication count)
- Email templates and tone
- Sending schedules and rate limits
- Response tracking and follow-up intervals

### Future Enhancements

- Integration with university admission portals
- Automated CV/SOP customization for each professor
- Machine learning model to predict response likelihood
- Browser extension for one-click professor analysis
- Integration with LinkedIn and ResearchGate profiles
- Response sentiment analysis and recommendation engine

### Real-World Impact

This project emerged from personal experience applying to PhD programs, where I contacted over 200 professors manually. By automating the tedious parts while maintaining genuine personalization, this tool helps aspiring PhD students focus on what matters: finding the right advisor match and preparing strong applications.

**Note**: This tool is intended to assist with genuine academic outreach. Users should ensure all communications comply with university policies and email best practices.
