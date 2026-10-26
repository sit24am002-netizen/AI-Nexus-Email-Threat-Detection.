
# Technical Design Document
## AI Nexus – Email Threat Detection

### 1. Introduction

AI Nexus is a web-based prototype designed to identify suspicious email characteristics and help users understand potential email threats.

The current implementation is a frontend application using HTML, CSS, and JavaScript. It performs rule-based analysis and displays risk indicators.

### 2. System Architecture

```text
+----------------------+
|         User         |
+----------------------+
           |
           v
+----------------------+
|   Web User Interface |
|      HTML + CSS      |
+----------------------+
           |
           v
+----------------------+
|   JavaScript Logic   |
|  Email Input & Rules |
+----------------------+
           |
           v
+----------------------+
| Risk Score and       |
| Warning Indicators   |
+----------------------+
           |
           v
+----------------------+
| Dashboard and Results|
+----------------------+
```

### 3. Technology Stack

- HTML5: structures the interface.
- CSS3: provides styling and layout.
- JavaScript: handles interactions and rule-based email analysis.
- Web Speech API: supports browser-based voice alerts where available.
- GitHub: hosts the source code and project documentation.

### 4. Main Components

**4.1 User Interface**

Provides the inbox, analyzer, dashboard, history, and reports sections.

**4.2 Email Input**

Accepts email subject and message content for analysis.

**4.3 Rule-Based Analyzer**

Checks email content against predefined indicators, such as suspicious phrases and URL-related patterns.

**4.4 Risk Display**

Displays the calculated score, risk category, and warning indicators.

**4.5 Demo Monitoring**

Uses predefined sample emails to simulate incoming email activity.

**4.6 Voice Alerts**

Uses browser speech synthesis to announce supported alerts.

### 5. Data Flow

1. The user selects a sample email or enters email content.
2. The application receives the available email fields.
3. JavaScript evaluates the content using predefined rules.
4. The application calculates a heuristic score.
5. The result is mapped to the interface's risk classification.
6. The user reviews the result and warning indicators.

### 6. Current Implementation

The current prototype uses rule-based detection and predefined sample data.

It does not currently implement:
- A trained machine-learning model.
- TF-IDF feature extraction.
- A backend prediction API.
- Real Gmail OAuth authentication or API access.
- A persistent database.
- Automated security verification of attachments.

These capabilities may be introduced in future versions.

### 7. Security Considerations

- Do not store passwords, API keys, or OAuth secrets in frontend code.
- Treat email content and URLs as untrusted input.
- Avoid opening suspicious links or attachments during testing.
- Validate inputs before processing them.
- Use secure authentication and server-side controls for future integrations.
- Do not use the prototype as the sole protection against real email threats.

### 8. Future Architecture

A future version may contain:

1. A frontend application.
2. A secure backend API.
3. A trained email classification model.
4. A URL reputation service.
5. Secure Gmail API integration using OAuth.
6. A database for authorized, appropriately protected analysis records.
7. Automated tests and model evaluation.

### 9. Conclusion

AI Nexus demonstrates a basic workflow for email threat awareness through a web interface and rule-based analysis. Its modular structure can be extended with machine learning, secure integrations, and more comprehensive testing.
