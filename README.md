# CaseFile-AI
# True Crime Investigator – AI-Powered Case Summarizer

## Overview

True Crime Investigator is an AI-powered platform designed to quickly generate detailed summaries of real-world true crime cases. This project aims to make it easier for researchers, students, and enthusiasts to explore, understand, and analyze complex true crime cases by using advanced generative AI (Google Gemini 2.0 Flash) to summarize and structure information.

Users can generate:

- Structured Timelines of events
- Victim/Suspect Profiles
- Grounded Facts sourced from Wikipedia
- JSON-based Case Files
- Interactive Q&A Assistants for case-related queries

This platform automates the summarization process, making case summaries report-ready and exportable in multiple formats (.json, .txt, .pdf).
![image](https://github.com/user-attachments/assets/e6be9718-ea1f-4eef-ab7b-9033fef5d333)

## Features

- **AI Case Summarization**: Generates structured case reports including timelines, profiles, facts, and theories.
- **Interactive Q&A**: Ask any questions related to a case and get natural language answers.
- **Efficient Case Lookup**: Supports fuzzy matching and lookup from a curated database of famous cases.
- **Export Options**: Export case reports as .json, .txt, or .pdf files.
- **Session Memory**: Displays the last 3 searched cases for quick access.
- **Smart Suggestions**: When no exact match is found, the system suggests related cases using Gemini-powered suggestions.
- **Read More**:The genres are categorized, and each category lists famous cases associated with it.

## Use Cases

- **Research Assistance**: Quickly generate structured summaries for research or studies.
- **True Crime Enthusiasts**: Get in-depth details about famous cases and theories.
- **Students**: Aid in writing essays, reports, or presentations related to real-world crime cases.
- **Journalists**: Collect and organize case details for articles or investigative reports.

## Features Breakdown

### 1. Case Summarization

The main functionality of the platform is to generate detailed case reports. For each input (e.g., "JonBenét Ramsey"), the system uses Google Gemini 2.0 Flash to pull relevant case data and summarize it. The output includes:

- Timeline of Events
- Victim/Suspect Profiles
- Public Theories
- Legal Outcomes
- Media Coverage
- References

### 2. Q&A Interface

Once a case report is generated, users can ask detailed questions about the case, and the AI will answer based on the report. Questions such as:

- "Who were the suspects?"
- "What’s the timeline?"
- "Were there any theories?"

### 3. Case Lookup & Matching

The system performs case lookup using three stages:

- **Exact Match**: Checks for the exact case name in a curated list.
- **Fuzzy Match**: Uses fuzzy string matching to suggest cases that might match the user input (e.g., “Jon” → “JonBenét Ramsey”).
- **Gemini Suggestions**: If no match is found, the AI suggests closely related cases.

### 4. Smart Disambiguation

The Local Case Index (CASE_LIST) contains a curated list of famous cases. This makes the lookup process faster and helps avoid unnecessary calls to the LLM.

### 5. Export Options

Generate and export reports in different formats:

- **.json**: For data integration or programmatic use.
- **.txt**: For readable, text-based reports.
- **.pdf**: For polished, presentation-ready reports.

### 6. User Interface with Gradio

The interface is built using Gradio to allow non-technical users to easily interact with the system. It features:

- A Textbox to input case names or keywords.
- Interactive Buttons for case suggestions, Q&A, and export options.
- File export options (.json, .txt, .pdf).
- Recent search memory to quickly navigate back to previously viewed cases.

## System Flow

1. **User Input**: User provides the case name or keyword.
2. **Case Lookup**: The system checks if the case exists in the local database (CASE_LIST).
3. **Data Generation**: If no exact match is found, the system generates a detailed JSON report by querying Google Gemini 2.0.
4. **Report Generation**: The report is structured and rendered as a markdown summary.
5. **Q&A**: The user can ask questions about the generated report, and the AI will answer based on the report content.
6. **Export**: The user can export the case summary as a JSON, text, or PDF file.
![Screenshot 2025-06-14 165042](https://github.com/user-attachments/assets/f215dead-b1e0-4df4-acf1-ed1e96db7bab)
![Screenshot 2025-06-14 165100](https://github.com/user-attachments/assets/f2e10b97-bfef-4719-a1fb-dbe795d29e55)
![Screenshot 2025-06-14 165133](https://github.com/user-attachments/assets/a51e76f8-8cae-4648-895a-27ee9a8e89ad)
![Screenshot 2025-06-14 165208](https://github.com/user-attachments/assets/596e728a-b8c7-4617-98aa-84ebfc658305)
![Screenshot 2025-06-14 165242](https://github.com/user-attachments/assets/36cd7ca0-ffc9-4381-abef-9a87e1d3554d)

![image](https://github.com/user-attachments/assets/dbf25367-2aec-4626-84ac-d9b6e759ab77)



How to Use
Step-by-Step Workflow

    Enter a Case Name or Keyword: Type the case name (e.g., "JonBenét Ramsey") or a keyword related to the case.

    AI Report Generation: The AI will automatically generate a detailed case summary.

    Ask Questions: Once the report is generated, use the Q&A section to ask specific questions about the case.

    Export the Report: After reviewing the case summary, you can export the report in your preferred format (JSON, TXT, or PDF).

Example Use Cases

    Case Search: Type "JonBenét Ramsey" → The system will generate a summary of the case.

    Case Q&A: Ask, “Who were the suspects?” after generating the summary.

    Case Export: Export the summary to a PDF for presentation.

Data Sources

    Wikipedia: Case details are pulled from reliable sources like Wikipedia.

    User-Provided Input: If no case is found, the system generates suggestions based on user input.

Export Module

You can export the generated summaries to:

    JSON: For data integration or sharing.

    Text: For readable text-based files.

    PDF: For printable, presentation-ready documents.

Read More Feature: Explore Popular Crime Genres

We added a "Read More" feature to explore popular true crime cases within different genres. The genres are categorized, and each category lists famous cases associated with it.


Each genre section will allow users to view a list of popular cases, with links to detailed case summaries and timelines.
Advanced Functionality

    Agent Decision Flow: Ensures that the system reacts to user input intelligently by combining exact matches, fuzzy matching, and AI suggestions.

    Gradio Memory: The system stores the last 3 searched cases to provide context for future queries.

    Gradio UI: Allows easy interactions via a clean and simple interface.
