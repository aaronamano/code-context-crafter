# Content Processing Pipeline

This document describes a step-by-step content processing pipeline for handling user-input documentation or best practices content.

## Pipeline Steps

### 1. **Start**
   - **Process Initiation**

### 2. **URL Input**
   - **Input:** User provides documentation or best practices video URL
   - **Action:** Accept URL input from user

### 3. **Validator**
   - **Check:** Verify if URL exists and has proper format
   - **Action:** Validate URL accessibility and structure

### 4. **Classifier**
   - **Determine:** Media type classification
   - **Options:**
     - Video
     - Text/Code
   - **Action:** Identify content type for routing

### 5. **Router**
   - **Route:** Direct content based on classification
   - **Branches:**
      - Video → ContentProcessor
      - Text → ContentProcessor
   - **Note:** Both paths lead to the unified ContentProcessor

### 6. **ContentProcessor** (Unified Node)
   - **Combined Functionality:** Scraping, Cleaning, and Enhancement
   - **Step 1 - Scraping:**
     - **Tool:** Firecrawl API
     - **Action:** Scrape content from URL
     - **Output:** Markdown formatted result
   - **Step 2 - Cleaning:**
     - **Action:** Clean markdown result
     - **Goal:** Maintain relevant content while removing noise
   - **Step 3 - Enhancement:**
     - **Action:** Enhance content with additional information
     - **Add:** Best practices, "do vs don't" guidelines, especially for specific use cases

## Flow Summary
Start → URL Input → Validator → Classifier → Router → ContentProcessor


## Implementation Notes
- Both video and text/code content types follow the same path after classification
- Firecrawl API is used for content extraction
- Final output is saved locally as a markdown file