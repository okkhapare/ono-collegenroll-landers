# Degree Match Quiz Flowchart

## Manager Review Version

```mermaid
flowchart TD
  Start([Start quiz])

  Q1["Q1: Learner stage"]
  Q2["Q2: Field of interest"]
  Q3["Q3: Highest completed qualification"]
  Q4["Q4: Main goal"]
  Q5["Q5: Credential level"]
  Q6["Q6: Weekly study time"]
  Q7["Q7: Budget"]
  Q8["Q8: Years of work experience"]
  Lead["Lead gate: name, email, optional phone"]
  Results["Top 3 program matches"]

  Start --> Q1
  Q1 --> Q2
  Q2 --> Q3
  Q3 --> Q4
  Q4 --> Q5
  Q5 --> Q6
  Q6 --> Q7
  Q7 --> StageCheck{"Student learner stage?"}
  StageCheck -->|"Yes"| Lead
  StageCheck -->|"No"| Q8
  Q8 --> Lead
  Lead --> Results

  Q1 -. "filters available qualification choices" .-> Q3
  Q1 -. "filters available main goal choices" .-> Q4
  Q1 -. "controls whether work experience is shown" .-> StageCheck

  Q3 -. "filters available credential levels" .-> Q5
  Q4 -. "if goal = Transfer credits, narrows credential levels" .-> Q5
```

## How To Read It

Solid arrows show the screen order users move through.

Dotted arrows show where an earlier answer changes later options.

The quiz is mostly linear. The main branching behavior is filtering, not sending users into separate paths.

## Branch Detail

```mermaid
flowchart TD
  Learner["Learner stage"]
  Qualification["Qualification choices"]
  Motivation["Main goal choices"]
  Experience{"Show work experience?"}

  Learner --> Qualification
  Learner --> Motivation
  Learner --> Experience

  Experience -->|"High school, community college, undergraduate, graduate student"| Skip["Skip work experience"]
  Experience -->|"Early career, mid career, changing careers, returning learner"| Ask["Ask years of experience"]

  Qualification --> Credential["Credential level choices"]
  Motivation --> Transfer{"Main goal = Transfer credits?"}
  Transfer -->|"Yes"| TransferLevels["Only Associate, Bachelor's, Not sure"]
  Transfer -->|"No"| Credential
```

## Manager Review Questions

1. Should graduate students skip the work-experience question?
2. Should Transfer credits limit users to Associate, Bachelor's, and Not sure only?
3. Are Returning learners allowed to choose Start college?
4. Do we want a fallback message if a selected category has fewer than three close online matches?

All offered programs are treated as online, so the quiz no longer asks separate delivery or regional preference questions.

## Code Pointers

- Questions and option lists: `degree-match/index.html`, around `const QUESTIONS`
- Branch/filter rules: `degree-match/index.html`, around `const OPTION_FILTERS`
- Visible-question logic: `getVisibleQuestions()`
- Filtered-option logic: `getFilteredOptions()`
- Downstream answer reset: `clearDownstreamAnswers()`
- Final scoring: `scoreProgram()`
