# EE-Profile Study Data

This repository contains de-identified supplementary data for the manuscript:

**EE-Profile: Structuring Life Narratives into Event-Enhanced Profile for Elder Care**

The data support the evaluation of EE-Profile, an event-enhanced profile representation for using older adults' life narratives in elder care. The public data package includes only materials that were de-identified and approved for public sharing. Raw audio recordings, consent forms, re-identification keys, unredacted transcripts, and participant-redacted sensitive content are not included.

## Recommended Upload Package

Upload these files/folders to the public repository:

- `README.md`: repository documentation.
- `Study1_Content_Check_Counts.csv`: coded Study 1 content-check counts reported in the manuscript.
- `Experiment_Summary.xlsx`: de-identified participant-level summary data for Studies 2-4.
- `1 narrative-elicitation interviews/`: narrative-collection prompt sheet and four public de-identified narrative transcripts.
- `profile/`: generated EE-Profile JSON files for the four public cases.
- `2 information retrieval tasks questions/`: Study 2 information-retrieval questions and answer keys for the four public cases.
- `one_page_summary/`: Study 3 one-page summary baselines for the four public cases.

Do not upload these local files as part of the data package:

- `返修版20260521_1900.pdf`: manuscript PDF, not a data file.
- `扩充实验汇总.xlsx` and `英文版.xlsx`: duplicate Chinese spreadsheet drafts. Use `Experiment_Summary.xlsx` for the public repository.
- Raw audio, consent forms, identity keys, unredacted transcripts, or any material that participants did not consent to share publicly.

## Repository Structure

```text
.
├── README.md
├── Study1_Content_Check_Counts.csv
├── Experiment_Summary.xlsx
├── 1 narrative-elicitation interviews/
│   ├── 1_narrative_interviews_prompt.xlsx
│   ├── 1_narrative_Mou.docx
│   ├── 1_narrative_Tao.docx
│   ├── 1_narrative_Wang.docx
│   └── 1_narrative_Zhang.docx
├── 2 information retrieval tasks questions/
│   ├── 2_information_retrieval_tasks_questions_mao.docx
│   ├── 2_information_retrieval_tasks_questions_tao.docx
│   ├── 2_information_retrieval_tasks_questions_wang.docx
│   └── 2_information_retrieval_tasks_questions_zhang.docx
├── one_page_summary/
│   ├── 张爷爷 One-page Summary.docx
│   ├── 汪爷爷 One-page Summary.docx
│   ├── 牟奶奶 One-page Summary.docx
│   └── 陶奶奶 One-page Summary.docx
└── profile/
    ├── 1/
    │   ├── narratives.json
    │   ├── entities.json
    │   └── events.json
    ├── 2/
    │   ├── narratives.json
    │   ├── entities.json
    │   └── events.json
    ├── 3/
    │   ├── narratives.json
    │   ├── entities.json
    │   └── events.json
    └── 4/
        ├── narratives.json
        ├── entities.json
        └── events.json
```

Note: `2_information_retrieval_tasks_questions_mao.docx` corresponds to the Mou case; the filename spelling is retained from the original data folder.

## Case Mapping

| Public case pseudonym | Narrative transcript | Profile folder | Retrieval task file | One-page summary | Profile contents |
|---|---|---|---|---|---|
| Wang | `1_narrative_Wang.docx` | `profile/1/` | `2_information_retrieval_tasks_questions_wang.docx` | `汪爷爷 One-page Summary.docx` | 52 narrative segments, 25 entities, 45 events |
| Tao | `1_narrative_Tao.docx` | `profile/2/` | `2_information_retrieval_tasks_questions_tao.docx` | `陶奶奶 One-page Summary.docx` | 63 narrative segments, 18 entities, 35 events |
| Zhang | `1_narrative_Zhang.docx` | `profile/3/` | `2_information_retrieval_tasks_questions_zhang.docx` | `张爷爷 One-page Summary.docx` | 40 narrative segments, 22 entities, 39 events |
| Mou | `1_narrative_Mou.docx` | `profile/4/` | `2_information_retrieval_tasks_questions_mao.docx` | `牟奶奶 One-page Summary.docx` | 32 narrative segments, 11 entities, 32 events |

## File Descriptions

### Narrative Elicitation Materials

`1 narrative-elicitation interviews/1_narrative_interviews_prompt.xlsx` contains the semi-structured interview prompt sheet used for collecting life narratives. The four narrative `.docx` files contain de-identified Chinese transcripts from the older adult participants who consented to public sharing.

### Generated EE-Profiles

Each `profile/<number>/` folder contains the generated EE-Profile data for one public case:

- `narratives.json`: de-identified and segmented narrative text. Main fields: `narrative_id`, `elder_id`, `text`, `events`.
- `entities.json`: extracted profile entities. Main fields: `entity_id`, `elder_id`, `entity_type`, `entity_name`, `entity_link_event`.
- `events.json`: event timeline entries. Main fields: `event_id`, `event_person`, `event_time`, `event_time_step`, `event_location`, `event_action`, `event_summary`, `event_link_narrative`, `event_link_entity`, `elder_id`.

Entity types include `education`, `occupation`, `achievement`, `health`, and `interest`. Event entries link back to narrative segment IDs and entity IDs.

### Study 1 Content Check

`Study1_Content_Check_Counts.csv` contains the per-profile counts used for the Study 1 content-check results. Columns include the number of extracted entities and events and participant-marked issue counts for wrong entity, wrong event fact, wrong time, wrong location, and wrong person/actor.

### Study 2 Retrieval Efficiency and Workload

`2 information retrieval tasks questions/` contains the information-retrieval questions and answer keys used in Study 2. Each file corresponds to one public case.

In `Experiment_Summary.xlsx`:

- `Study 2 Retrieval Efficiency` contains de-identified participant-level accuracy, task time, and case assignment data for raw narrative and EE-Profile conditions (`n = 31`).
- `Study 2 Workload` contains de-identified participant-level Raw NASA-TLX item responses for raw narrative and EE-Profile conditions (`n = 31`). The spreadsheet stores item values on a 0-5 coding scale; manuscript tables report the corresponding 0-100 values after multiplying by 20.

### Study 3 Conversation Preparation

`one_page_summary/` contains the one-page summary baselines used in Study 3. These summaries were prepared from the same narrative corpus as the EE-Profile and raw narrative conditions.

In `Experiment_Summary.xlsx`, `Study 3 Conversation` contains de-identified participant-level ratings for willingness, confidence, and perceived usefulness across raw narrative, EE-Profile, and one-page summary conditions (`n = 31`).

### Study 4 Usability and Profile Authoring

In `Experiment_Summary.xlsx`:

- `Study 4 SUS` contains System Usability Scale item responses. Complete SUS responses are available for 29 participants; IDs 18 and 20 are incomplete.
- `Study 4 Profile Creation Time` contains participant-level mean narrative entry time, extraction latency, and post-editing time for speech and text input. Complete authoring logs are available for 29 participants; IDs 18 and 20 are incomplete.

## Privacy and Data Handling

The public files are de-identified, but life-narrative data can still contain potentially identifiable combinations of age, occupation, locations, health history, and life events. Before public release, confirm that all names used in filenames and file contents are pseudonyms rather than real names, and verify that no direct identifiers remain.

The following materials are intentionally not publicly released:

- Raw audio recordings.
- Consent forms and identity keys.
- Unredacted transcripts.
- Content redacted by participants during member checking.
- Materials from participants who did not consent to public sharing.

## Suggested Data Availability Statement

De-identified narratives and generated EE-Profiles for the four older-adult participants who consented to public sharing, Study 2 task materials, Study 3 one-page summary baselines, Study 1 coded content-check counts, and de-identified participant-level summary data for Studies 2-4 are publicly available at: **https://github.com/gerontech-hfut/EE-Profile**.

Raw audio recordings, consent forms, re-identification keys, unredacted transcripts, participant-redacted sensitive content, and materials from participants who did not consent to public sharing are not publicly available to protect participant privacy. Requests for restricted materials may be directed to the corresponding author and will be considered subject to participant consent and ethics approval.

## Citation

If you use these materials, please cite the associated manuscript:

Li, Y., Yang, J., Zhou, J., Chen, H., & An, N. (2026). *EE-Profile: Structuring Life Narratives into Event-Enhanced Profile for Elder Care*.
