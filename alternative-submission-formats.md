# Alternative Submission Formats for Pre-Lab Assignments

## Introduction

This document outlines various submission formats that could supplement or replace traditional R Markdown (.Rmd) submissions for pre-lab assignments. These alternatives can help accommodate different learning styles, build professional skills, and prepare students for real-world data journalism work.

## Current Format

Students currently work in R Markdown notebooks where they:
- Run code in chunks
- Answer questions in text format below each task
- Submit completed .Rmd files

## Alternative Submission Formats

### 1. Video Walkthroughs

**Format**: 5-10 minute screencast video (MP4, MOV)

**What it would look like**:
- Students record their screen while working through the pre-lab
- Narrate their thought process as they run code and analyze results
- Explain what each code chunk does in their own words
- Point out interesting findings or challenges encountered
- Can use free tools like Loom, OBS Studio, QuickTime, or built-in screen recording

**Best for**:
- Pre-lab 8 (Data Visualization) - walking through chart creation decisions
- Pre-lab 12 (Web Scraping) - demonstrating the scraping process in real-time
- Pre-lab 5 (PDF Parsing) - showing the Tabula workflow

**Assessment criteria**:
- Clarity of explanation
- Demonstrated understanding of code functionality
- Quality of insights about the data
- Technical accuracy
- Audio quality and pacing

**Accessibility considerations**:
- Provide transcript or closed captions
- Allow script submission as alternative for students uncomfortable on camera
- Set maximum length to respect students' time

---

### 2. Audio Reflections/Podcasts

**Format**: Audio file (MP3, M4A, WAV) 3-8 minutes

**What it would look like**:
- Students record voice memos discussing their findings
- Focus on insights rather than line-by-line code review
- Structure like a mini data journalism story or podcast segment
- Could include an intro, findings, methodology note, and conclusion
- Record using phone, computer microphone, or podcast apps like Anchor

**Best for**:
- Pre-lab 2 (Mutate/Filter) - explaining patterns found in Maryland election data
- Pre-lab 3 (Data Cleaning) - discussing data quality issues discovered
- Final reflection questions (like Task 16 in pre-lab 2)

**Example structure**:
1. Introduction: "I analyzed Maryland campaign expenditure data and discovered..."
2. Key finding: "The most surprising pattern was..."
3. Methodology note: "I used mutate and group_by to..."
4. Implications: "This matters because..."

**Assessment criteria**:
- Quality of data insights
- Understanding of analytical methods
- Storytelling and communication skills
- Ability to contextualize findings

---

### 3. Interactive HTML Reports

**Format**: HTML file with interactive elements

**What it would look like**:
- Students knit their R Markdown to HTML (already possible)
- Add interactive elements using plotly, DT, or leaflet packages
- Include collapsible code sections
- Add navigation/table of contents
- Host on GitHub Pages or submit as standalone HTML

**Best for**:
- Pre-lab 8 (Visualization) - create interactive charts
- Any pre-lab with geographic data - add interactive maps
- Complex data explorations where interactive filtering helps

**Enhanced features**:
```r
# Interactive table
library(DT)
datatable(maryland_expenses, filter = 'top')

# Interactive chart
library(plotly)
ggplotly(my_chart)
```

**Assessment criteria**:
- Functionality of interactive elements
- Design choices that enhance understanding
- Code quality and documentation
- Insights communicated through interactivity

---

### 4. Presentation Slides

**Format**: PDF or HTML slides (5-10 slides)

**What it would look like**:
- Students create slides using R Markdown (xaringan, ioslides, slidy)
- Present key findings and methodology
- Include selected code chunks and visualizations
- Tell a story with the data
- Could present live or record presentation

**Example slide structure**:
1. Title/Question
2. Data source and loading
3. Data cleaning steps
4. Key findings (with visualizations)
5. Code methodology
6. Conclusions/Next steps

**Best for**:
- Pre-lab 8 (Visualization) - showcase charts
- Pre-lab 3 (Data Cleaning) - before/after comparisons
- Any pre-lab asking "what did you discover?"

**Tools**:
- xaringan (professional presentations)
- Google Slides with R output screenshots
- Quarto presentations

---

### 5. Data Story Blog Posts

**Format**: Blog-style article (Markdown/HTML)

**What it would look like**:
- Written in narrative journalism style
- Lead with findings, not methodology
- Embed visualizations and key code snippets
- Include methodology section at end
- Published on personal blog, Medium, or submitted as HTML

**Example structure**:
```
Headline: "Summer Months See Spike in Baltimore County Overdose Calls"

Lead: [Key finding from the data]

Nut graf: [Why this matters]

Body: [Supporting evidence from analysis with visualizations]

Methodology: [How the analysis was conducted]
```

**Best for**:
- All pre-labs, especially those with interesting findings
- Pre-lab 8 (Visualization) - tell visual stories
- Pre-lab 12 (Web Scraping) - present scraped data as news

**Assessment criteria**:
- Journalistic writing quality
- Effective data visualization integration
- Accuracy of analysis
- Clear methodology explanation
- News value and relevance

---

### 6. Code Annotation Videos (Silent Screencasts)

**Format**: Screen recording with text annotations (no audio)

**What it would look like**:
- Record screen while working through assignment
- Add text overlays/annotations explaining each step
- Use video editing software or tools like Descript
- Useful for students who prefer not to record audio
- Can add captions, arrows, highlights to emphasize points

**Best for**:
- Students who are ESL or have speech anxiety
- Complex coding sequences in pre-labs 3, 5, or 12
- Step-by-step demonstrations

**Tools**:
- iMovie, DaVinci Resolve (free)
- Camtasia, ScreenFlow (paid)
- Descript (automated captioning)

---

### 7. Jupyter-Style Observable Notebooks

**Format**: Interactive web notebook

**What it would look like**:
- Similar to R Markdown but with more interactivity
- Use Quarto for mixing R and other languages
- Readers can modify parameters and see results change
- Deploy to GitHub Pages or Quarto Pub

**Best for**:
- Advanced students who want to showcase technical skills
- Pre-lab 8 with interactive visualizations
- Creating portfolio pieces

---

### 8. Social Media Thread Format

**Format**: Text document structured as social media thread

**What it would look like**:
- Write findings as 5-10 tweet-length posts
- Each "tweet" covers one insight or step
- Include images of visualizations
- Practice communicating data findings concisely
- Submit as formatted document showing thread structure

**Example**:
```
🧵 Thread: What I learned analyzing MD campaign spending data

1/ I analyzed $X million in Maryland campaign expenditures
from 2022. Here's what stood out... [visualization]

2/ The biggest surprise: 65% of spending went to vendors
in just 3 states [chart]

3/ To clean this data, I had to standardize vendor names.
"ANEDOT" vs "Anedot" would have been counted separately
without str_to_upper()

4/ Methodology: Used R tidyverse, specifically mutate()
and group_by() to aggregate spending by state

5/ Key takeaway: [main finding and why it matters]
```

**Best for**:
- Practicing science communication
- Pre-labs with strong findings
- Building professional social media presence
- Students interested in data journalism communication

---

### 9. Comparative Analysis Reports

**Format**: PDF or HTML document

**What it would look like**:
- Students complete the pre-lab as normal
- Then compare their approach/findings with a partner
- Write up differences in methodology or interpretation
- Discuss why different approaches yielded different insights
- Requires peer collaboration

**Best for**:
- Pre-lab 3 (Data Cleaning) - different cleaning strategies
- Pre-lab 8 (Visualization) - different chart types for same data
- Teaching that analysis involves choices

---

### 10. Office Hours/Live Demos

**Format**: Live demonstration to instructor or TA

**What it would look like**:
- Student signs up for 10-15 minute session
- Walks instructor through their code live
- Answers questions about methodology
- Discusses findings in real-time
- Instructor provides immediate feedback

**Best for**:
- Students who excel at verbal explanation
- Accommodating students with writing difficulties
- Building presentation skills
- Office hours structure

---

## Hybrid Approaches

### Option A: Two-Part Submission
- Traditional .Rmd file (for code and technical work)
- PLUS one alternative format (for communication/presentation)
- Mirrors real newsroom work: analysis + public-facing story

### Option B: Choose Your Own Adventure
- Students select 2-3 pre-labs to submit in alternative formats
- Remaining pre-labs use traditional format
- Builds diverse portfolio

### Option C: Progressive Complexity
- Early pre-labs: traditional format (learn basics)
- Mid-semester: introduce alternative formats
- Final pre-labs: student choice of format

---

## Technical Considerations

### File Storage and Submission
- **LMS upload limits**: Most video/audio files are small enough (under 100MB)
- **Cloud storage**: Google Drive, Dropbox for larger files
- **GitHub**: For HTML, code, and rendered documents
- **YouTube/Vimeo**: For video hosting (can be unlisted)

### Accessibility Requirements
- Videos need captions/transcripts
- Audio needs transcripts
- Interactive elements need keyboard navigation
- Color choices need to be colorblind-friendly

### Time Investment
- Some formats (video editing) may take longer initially
- Others (audio reflection) may be faster than typing
- Consider allowing extra time for first alternative format submission

---

## Assessment Rubrics by Format

### Video Walkthroughs
- Technical accuracy (40%)
- Clarity of explanation (30%)
- Insight quality (20%)
- Production quality (10%)

### Audio Reflections
- Data insights (40%)
- Understanding of methodology (30%)
- Communication/storytelling (20%)
- Audio clarity (10%)

### Interactive HTML
- Functionality (30%)
- Code quality (30%)
- Design choices (20%)
- Insights communicated (20%)

### Data Story Blog Posts
- Journalistic quality (30%)
- Analytical accuracy (30%)
- Visualization effectiveness (20%)
- Methodology transparency (20%)

---

## Student Benefits

Different formats help students:
1. **Build diverse portfolios** for job applications
2. **Practice communication skills** beyond academic writing
3. **Accommodate different learning styles** and strengths
4. **Prepare for newsroom reality** (reporters often present findings verbally)
5. **Develop technical skills** (video editing, audio production, web publishing)
6. **Engage more deeply** with material through different modalities
7. **Reduce anxiety** for students who struggle with traditional writing

---

## Implementation Recommendations

### Start Small
- Introduce one alternative format for one pre-lab
- Gather student feedback
- Iterate and expand

### Make it Optional First
- Allow alternative formats as bonus/extra credit
- Build student comfort before requiring them

### Provide Examples
- Create sample submissions in each format
- Show what excellence looks like

### Offer Technical Support
- Provide tutorials for recording tools
- Hold workshops on video/audio creation
- Create templates for different formats

### Set Clear Expectations
- Provide rubrics for each format type
- Specify required elements
- Give length/time guidelines

---

## Questions for Further Consideration

1. Should alternative formats replace or supplement traditional submissions?
2. How do we ensure equity if some formats require more technical resources?
3. Should students get to choose formats, or should they be assigned?
4. How can peer review work with non-text submissions?
5. What's the archival strategy for audio/video submissions?
6. How do alternative formats prepare students for data journalism careers?

---

## Conclusion

Alternative submission formats can enrich pre-lab assignments by:
- Developing professional communication skills
- Accommodating diverse learning styles
- Building portfolio materials
- Making data journalism education more engaging
- Reflecting real-world newsroom work

The key is thoughtful implementation that maintains academic rigor while expanding how students demonstrate learning and communicate findings.
