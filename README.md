# EE-Profile Public Data

This repository contains de-identified study materials and participant-level summary data for EE-Profile.

Repository URL: https://github.com/gerontech-hfut/EE-Profile

## Contents

```text
.
├── README.md
├── Study1_Content_Check_Counts.csv
├── Experiment_Summary.xlsx
├── 1 narrative-elicitation interviews/
├── 2 information retrieval tasks questions/
├── 3 one_page_summary/
└── 4_profile/
```

## File Overview

| Path | Description |
|---|---|
| `Study1_Content_Check_Counts.csv` | Per-profile content-check counts for extracted entities, events, and marked issues. |
| `Experiment_Summary.xlsx` | De-identified participant-level summary data for retrieval efficiency, workload, conversation ratings, SUS responses, and profile-creation time. |
| `1 narrative-elicitation interviews/` | Interview prompt sheet and four de-identified narrative transcripts. |
| `2 information retrieval tasks questions/` | Information-retrieval task questions and answer keys for the four public cases. |
| `3 one_page_summary/` | One-page summary baselines for the four public cases. |
| `4_profile/` | Generated EE-Profile JSON files for the four public cases. |

## Case Mapping

| Case | Narrative transcript | Retrieval task | One-page summary | EE-Profile folder |
|---|---|---|---|---|
| Mou | `1 narrative-elicitation interviews/1_narrative_Mou.docx` | `2 information retrieval tasks questions/2_information_retrieval_tasks_questions_mou.docx` | `3 one_page_summary/3_Mou_One-page Summary.docx` | `4_profile/4_Mou/` |
| Tao | `1 narrative-elicitation interviews/1_narrative_Tao.docx` | `2 information retrieval tasks questions/2_information_retrieval_tasks_questions_tao.docx` | `3 one_page_summary/3_Tao_One-page Summary.docx` | `4_profile/4_Tao/` |
| Wang | `1 narrative-elicitation interviews/1_narrative_Wang.docx` | `2 information retrieval tasks questions/2_information_retrieval_tasks_questions_wang.docx` | `3 one_page_summary/3_Wang_One-page Summary.docx` | `4_profile/4_Wang/` |
| Zhang | `1 narrative-elicitation interviews/1_narrative_Zhang.docx` | `2 information retrieval tasks questions/2_information_retrieval_tasks_questions_zhang.docx` | `3 one_page_summary/3_Zhang_One-page Summary.docx` | `4_profile/4_Zhang/` |

## EE-Profile JSON Files

Each case folder in `4_profile/` contains:

| File | Main fields |
|---|---|
| `narratives.json` | `narrative_id`, `elder_id`, `text`, `events` |
| `entities.json` | `entity_id`, `elder_id`, `entity_type`, `entity_name`, `entity_link_event` |
| `events.json` | `event_id`, `event_person`, `event_time`, `event_time_step`, `event_location`, `event_action`, `event_summary`, `event_link_narrative`, `event_link_entity`, `elder_id` |

Entity types are `education`, `occupation`, `achievement`, `health`, and `interest`.

## EE-Profile Case Counts

| Case folder | Narrative segments | Entities | Events |
|---|---:|---:|---:|
| `4_profile/4_Mou/` | 32 | 11 | 32 |
| `4_profile/4_Tao/` | 63 | 18 | 35 |
| `4_profile/4_Wang/` | 52 | 25 | 45 |
| `4_profile/4_Zhang/` | 40 | 22 | 39 |

## Experiment Summary Workbook

`Experiment_Summary.xlsx` contains five sheets:

| Sheet | Description |
|---|---|
| `Study 2 Retrieval Efficiency` | Accuracy, task time, and case assignment for raw narrative and EE-Profile conditions. |
| `Study 2 Workload` | Raw NASA-TLX item responses for raw narrative and EE-Profile conditions. |
| `Study 3 Conversation` | Willingness, confidence, and usefulness ratings for raw narrative, EE-Profile, and one-page summary conditions. |
| `Study 4 SUS` | System Usability Scale item responses. |
| `Study 4 Profile Creation Time` | Entry time, extraction latency, and post-editing time for speech and text input. |

