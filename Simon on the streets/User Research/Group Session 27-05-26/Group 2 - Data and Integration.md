# Mastek4Good — Workshop 2: Data and Integration
**Date:** 27 May 2026

A huge thanks to all of the excellent and highly engaged participants in Workshop 2 this evening — and a particular thank you to Tracey for patiently answering all of the questions she was bombarded with!

## Areas of Focus

From a data and integration perspective we identified four areas of focus.

### 1. Salesforce ('Inform') — System of Record

The core system of record and official store of all client personal data. The Simon on the Streets team have enhanced this a little, but the underlying data structures and data entry forms are inherited legacies that are not a match for what SotS actually need.

### 2. Data Capture

The interfaces through which SotS staff capture client information and log events. This currently consists of a set of forms within Inform (Salesforce) and a mobile app that offers cut-down functionality, making it not fit for purpose for use in the field.

Tracey highlighted that all interactions with clients and all tasks undertaken in supporting them (e.g. gave advice, undertook welfare check, visit to GP, completed benefits form) should be captured. At present, all of these tasks are shown as individual checkboxes on a single form, allowing case workers to record multiple events in a single submission. However this form is large and complex, does not timestamp individual tasks, and has a single notes field in which notes associated with any of the tasks are compiled together.

It was proposed that the user experience could be greatly simplified if individual tasks could be captured with their own associated notes, saved and timestamped individually.

### 3. Application of Data

The use of client data held in Inform to partially or fully populate third-party forms (typically government forms). This is currently done manually, and Inform holds only a small amount of the information typically needed.

### 4. Reporting

SotS have significant issues generating reports from their data that provide the insights they require. They have spent significant effort tailoring their data capture to support more effective reporting, but this remains clunky and bespoke reporting requirements frequently require a request to Salesforce, which can take multiple days to fulfil.

## Key Observations

**Data quality and structure:** The ways in which data is captured and stored leads to poor data quality and gets in the way of extracting it in the ways SotS want to, whether for reporting or for utilising it to fill in downstream forms. In particular, a significant amount of the information captured is entered as unstructured free text in notes fields.

**User journey mapping:** The exercise undertaken to map out existing user journeys was valuable in highlighting pain points and underlining the need for change. However, these journey maps don't capture what *good* looks like — i.e. the ideal user journeys for SotS staff for different use cases and under different circumstances.

**Working within Salesforce:** Salesforce provides significant scope for customising the data fields captured and the forms used to capture them. It may therefore be possible to adapt both the data schema and the data capture user experience(s) within the platform SotS already have. If there is a clear path forward, this may be preferable to building and migrating to something new.

**Salesforce APIs:** Salesforce provides a rich suite of APIs that should permit external applications to post or retrieve information to/from Salesforce — in principle enabling any external tools we might build to interface with Salesforce directly and removing the need for manual re-keying. However, it is not yet clear whether API access is permitted on SotS's current package, or whether there would be cost implications to enabling or using it.

**Data governance:** Storing PII and sensitive data in platforms other than Salesforce increases data control complexity and should only be done minimally and where necessary, in line with GDPR.

**Design principles:** Any changes made should be kept simple and must do no harm to existing capabilities.

## A Potential Innovation: Voice Memo Capture

Whilst the session was primarily focused on the problem domain, one potential solution concept was briefly discussed: the idea that an interaction could be captured as a secure voice memo in the field and then automatically transcribed, parsed, and uploaded to Salesforce. Tracey felt this could be a really excellent user experience for case workers, so it would be great to explore whether this is a viable data capture method.

## Proposed Workstreams for Mastek4Good

| # | Workstream | Description | Suggested Skillset |
|---|------------|-------------|--------------------|
| 1 | **User Journey Mapping** | Facilitate an exercise to map out key user journeys ('jobs to be done') for SotS staff, capturing what needs to be done and the data to be captured — deliberately without considering what the technology solution looks like today or might look like in the future. | BA / Product Manager / UX Designer |
| 2 | **Target Data Architecture** | Building on the journey mapping, review data and functionality requirements to design a target data architecture/schema for SotS. This would be useful both as a target for adapting the existing Salesforce solution and as a foundation for any future alternative solution. | Data Scientist / Data Analyst / DB Architect / BA |
| 3 | **Salesforce Customisation Review** | Investigate what options exist within Salesforce for end users with appropriate privileges to customise the data structure and forms — including a review of what can be customised in the mobile app. | Ideally someone with Salesforce experience, but could be approached from first principles by someone interested in learning |
| 4 | **Data Capture Workflow Design** *(conditional on Workstream 3)* | If it is determined that the data structure and form workflows can be changed within Salesforce, design new data capture workflows that deliver an optimum experience for SotS, building on the journey mapping work. | UX Designer |
| 5 | **Salesforce API Investigation** | Investigate what API functionality is available specifically for the Salesforce Inform solution, documenting available functionality and any commercial implications. | Solution Architect / Software Engineer |
