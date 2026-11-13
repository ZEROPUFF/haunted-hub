# Requirements — Haunted Hub

## Introduction
A single-page Halloween dashboard for one user (zeropuff) to find free tools, domains and daily deals fast, with a built-in EXAONE AI assistant.

## Requirements

### Requirement 1: Searchable tool directory
**User Story:** As the user, I want to search my free tools and domains, so I can open the right one in seconds.
#### Acceptance Criteria
1. WHEN the page loads, THEN it SHALL show at least 12 real tool/domain cards with name, description, tag and link.
2. WHEN the user types in the search box, THEN the list SHALL filter by name, description or tag.
3. WHEN a card is clicked, THEN it SHALL open in a new tab.

### Requirement 2: EXAONE panel (local key only)
**User Story:** As the user, I want to ask EXAONE questions from the dashboard, so I don't have to switch apps.
#### Acceptance Criteria
1. WHEN the user enters an API key, THEN it SHALL be stored only in browser localStorage, never in the repo or sent elsewhere.
2. WHEN the user asks a question, THEN the app SHALL POST to https://api.exaone.ai/v1/chat/completions with model k-exaone_v2.5 and show the reply.
3. WHEN the call fails, THEN the app SHALL show the status/error and the exact request to retry elsewhere.

### Requirement 3: Deals feed
**User Story:** As the user, I want today's deals, so the dashboard stays useful daily.
#### Acceptance Criteria
1. WHEN the page loads, THEN it SHALL try the public 线报酷 feed and show up to 5 items.
2. WHEN the live feed is blocked, THEN it SHALL show sample deals and explain why.

### Requirement 4: Kiroween compliance
**User Story:** As the entrant, I want the repo to satisfy Kiroween rules, so the submission is eligible.
#### Acceptance Criteria
1. WHEN the repo is inspected, THEN the root SHALL contain a `.kiro` directory with this spec.
2. WHEN the project is judged, THEN it SHALL be identifiable as Costume Contest: a polished, spooky UI that helps the app work.
