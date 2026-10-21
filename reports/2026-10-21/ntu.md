# Nanyang Technological University (NTU) · usability audit · 2026-10-21

Pages read: home https://www.ntu.edu.sg/ (ok, HTTP 200, 209 ms, 156 KB) ·
admissions https://www.ntu.edu.sg/admissions (ok, HTTP 200, 205 ms, 140 KB)
robots.txt: rules read (group "*"); both pages allowed.

## Heuristics

| # | Heuristic | Severity | Evidence from the HTML |
|---|---|---|---|
| 1 | Visibility of system status | 1 | `home:breadcrumbs.present` = true; `admissions:breadcrumbs.present` = true; `home:navigation.aria_current_count` = 0; `admissions:navigation.aria_current_count` = 0; `home:http.response_ms` = 209; `admissions:http.response_ms` = 205 |
| 2 | Match between system and the real world | 1 | `home:navigation.landmarks.0.top_level_links.0` = "About Us"; `home:navigation.landmarks.0.top_level_links.5` = "Life at NTU"; `home:navigation.landmarks.1.top_level_links.0` = "Corporate NTU"; `home:lang` = "en" |
| 3 | User control and freedom | 2 | `home:carousel_or_slider_hints` = 19; `admissions:carousel_or_slider_hints` = 12; `home:autoplay_media` = 0; `home:skip_link.present` = false; `home:navigation.home_links` = 2 |
| 4 | Consistency and standards | 2 | `home:headings.h1_count` = 0; `admissions:headings.h1_count` = 0; `home:landmarks.main` = false; `admissions:landmarks.main` = false; `home:images.missing_alt` = 0; `home:forms.inputs_without_label` = 1 |
| 5 | Error prevention | 1 | `home:forms.inputs_without_label` = 1; `home:forms.unlabelled_with_placeholder_only` = 1; `admissions:forms.unlabelled_with_placeholder_only` = 1; `admissions:forms.inputs` = 38 |
| 6 | Recognition rather than recall | 0 | `home:links.vague_text_total` = 0; `admissions:links.vague_text_total` = 0; `home:search.search_input` = true; `admissions:search.search_input` = true; `home:breadcrumbs.present` = true |
| 7 | Flexibility and efficiency of use | 2 | `home:skip_link.present` = false; `admissions:skip_link.present` = false; `home:navigation.landmarks.0.links` = 303; `home:search.search_form` = true; `home:meta_viewport` = "width=device-width, initial-scale=1.0" |
| 8 | Aesthetic and minimalist design | not judged | not judged from HTML: whether the page is crowded is a visual question; the HTML gives only counts such as `home:navigation.landmarks.0.links` = 303 and `home:visible_word_count` = 1437. |
| 9 | Help users recognise, diagnose and recover from errors | not judged | not judged from HTML: no error messages or failed states appear on these pages. |
| 10 | Help and documentation | 0 | `home:help_faq_contact_links.0` = "Frequently Asked Questions"; `home:help_faq_contact_links.1` = "Contact Us"; `home:footer_contact.phone_pattern` = true; `home:footer_contact.postal_address_pattern` = true; `admissions:help_faq_contact_links.2` = "Contact Service Desk" |

Severity: 0 no problem, 1 cosmetic, 2 minor, 3 major, 4 severe (see HEURISTICS.md). Lower is better.

## Three suggestions for the web team
1. **Page heading and main area on every page · Consistency and standards.** Give each page one `h1` heading and wrap the central content in a `main` landmark. Both pages report no `h1` and no `main`, so screen reader users cannot jump to the page title or the content.
2. **Start of the page, before the 303-link menu · Flexibility and efficiency of use.** Add a "Skip to main content" link as the first focusable item. Keyboard users now have to pass the whole menu on every page.
3. **The text field with a placeholder only (probably the search box) · Error prevention.** Add a visible or screen-reader label. A placeholder disappears when someone types, and a label also helps assistive technology.

## Since last week
First audit; nothing to compare yet.

## Limits
Judged from the HTML of two pages only. Visual design, colour contrast and real tasks were not judged.
These findings are prompts for a human evaluator, not verdicts.
