# IPC to BNS 2023 Section Mapping (India)

A machine-readable mapping of **99 frequently cited sections of the Indian Penal Code, 1860 (IPC)** to their corresponding sections in the **Bharatiya Nyaya Sanhita, 2023 (BNS)**, which replaced the IPC with effect from **1 July 2024**.

Compiled by **Democrat Legal & Partners, Lucknow — https://democratlegal.com**

## Why this dataset exists

FIRs, judgments and textbooks written before 1 July 2024 cite IPC sections. Matters arising on or after that date cite BNS sections. Lawyers, students, journalists, police and developers constantly need to translate between the two. Courts still read pre-2024 precedents — for example, on cheating under IPC 420, now BNS 318(4) — so the old numbers remain in daily use.

The maxim *ignorantia juris non excusat* (ignorance of law is no excuse) assumes the law can be found. This dataset is a small contribution to making it easier to find.

## Files

| File | Description |
|---|---|
| `ipc-bns-mapping.csv` | 99 rows, UTF-8, comma-separated, header row included |
| `README.md` | This file |

## Columns

| Column | Description | Example |
|---|---|---|
| `ipc_section` | IPC section number | `420` |
| `ipc_title` | IPC section heading as given in the official table | `Cheating and dishonestly inducing delivery of property` |
| `bns_section` | Corresponding BNS section or sub-section. `Not retained (deleted)` where the official table marks the IPC section as deleted | `318(4)` |
| `bns_title` | Heading of the corresponding BNS section | `Cheating` |
| `notes` | `Marked "Change" in NCRB table` where the official table flags a change in the BNS provision; other short notes | — |

## Coverage

- Offences against the body (murder, culpable homicide, hurt, attempt, kidnapping, abduction)
- Offences against women and marriage (rape, outraging modesty, sexual harassment, stalking, voyeurism, dowry death, cruelty, bigamy)
- Property offences (theft, extortion, robbery, dacoity, misappropriation, criminal breach of trust, cheating, mischief, trespass)
- Forgery, criminal intimidation, defamation, conspiracy, abetment, attempt
- Offences relating to public servants, false evidence, public tranquillity, and the State
- 4 IPC sections marked "Deleted" in the official table (124A, 309, 377, 497)

## Source

All mappings were taken from the **official Corresponding Section Table of the Bharatiya Nyaya Sanhita, 2023** published by the **National Crime Records Bureau (Ministry of Home Affairs)** on its Sankalan portal:

- https://www.ncrb.mha.gov.in/uploads/SankalanPortal/SectionTableBNS.html (retrieved 18 Nov 2026)

The same table is published as a PDF by Uttar Pradesh Police:

- https://uppolice.gov.in/site/writereaddata/siteContent/Three%20New%20Major%20Acts/202406281710564823BNS_IPC_Comparative.pdf

Commencement date (1 July 2024): Press Information Bureau, https://pib.gov.in/PressReleasePage.aspx?PRID=2021352

## Method

1. The NCRB HTML table was downloaded and parsed row by row (IPC → BNS half of the table).
2. Where an IPC section maps to a BNS sub-section without its own heading (for example IPC 379 → BNS 303(2)), the heading of the parent BNS section was used in `bns_title`.
3. "(Change)" markers in the NCRB table are carried into `notes`.
4. No mapping was inferred or added from any other source.

## Limitations

- A corresponding section is **not always identical** in wording, ingredients or punishment. Rows marked "Change" in particular must be read against the bare text of the BNS.
- "Not retained (deleted)" means the official table lists the IPC section as deleted; where the BNS has a new provision on a related subject (for example BNS 152, or BNS 226), the NCRB table lists that as a **New Section**, not as a direct equivalent, and this dataset says so in `notes`.
- BNS 106(2) is listed in the NCRB table as not coming into force on 1 July 2024.
- This is a selection of 99 frequently cited sections, not the full IPC.

## Licence

**Creative Commons Attribution 4.0 International (CC BY 4.0)** — https://creativecommons.org/licenses/by/4.0/

You may share and adapt the data for any purpose, including commercial use, provided you give appropriate credit:

> IPC to BNS 2023 Section Mapping, compiled by Democrat Legal & Partners, Lucknow — https://democratlegal.com. Source: NCRB Corresponding Section Table of BNS 2023. Licensed CC BY 4.0.

## Disclaimer

This is general information, not legal advice. Always check the bare text of the BNS and the IPC, and the facts of your matter, before relying on any mapping.

## Contact

Democrat Legal & Partners (DLP)
Chamber No. 548, A Block, High Court, Vibhuti Khand, Gomti Nagar, Lucknow, Uttar Pradesh 226010
+91 81888 77758 | +91 90441 15555 | democratlegal@gmail.com
https://democratlegal.com
