# National University of Singapore (NUS) · usability audit · 2026-10-21

Pages read: home https://www.nus.edu.sg/ (ok, HTTP 200, 1887 ms, 70 KB) ·
admissions https://www.nus.edu.sg/admissions (bot_check_page, HTTP 200, 478 ms, 0 KB)
robots.txt: answered with an HTML page, not a rules file, so no rules apply (both pages).

## Heuristics

| # | Heuristic | Severity | Evidence from the HTML |
|---|---|---|---|
| 1 | Visibility of system status | 2 | `home:navigation.aria_current_count` = 0; `home:breadcrumbs.present` = true; `home:http.response_ms` = 1887; `home:http.bytes` = 72190 |
| 2 | Match between system and the real world | 1 | `home:navigation.landmarks.0.top_level_links.2` = "Education"; `home:navigation.landmarks.0.top_level_links.1` = "Admissions"; `home:headings.h2.0` = "Sidebar"; `home:lang` = null |
| 3 | User control and freedom | 2 | `home:carousel_or_slider_hints` = 9; `home:autoplay_media` = 0; `home:skip_link.present` = false; `home:navigation.home_links` = 13 |
| 4 | Consistency and standards | 3 | `home:headings.h1_count` = 0; `home:landmarks.main` = false; `home:lang` = null; `home:images.missing_alt` = 3; `home:links.empty_text` = 25; `home:forms.inputs_without_label` = 1 |
| 5 | Error prevention | 2 | `home:forms.inputs` = 1; `home:forms.inputs_without_label` = 1; `home:forms.unlabelled_with_placeholder_only` = 1 |
| 6 | Recognition rather than recall | 1 | `home:links.vague_text_total` = 3; `home:links.vague_text_by_phrase.learn more` = 3; `home:search.search_input` = true; `home:breadcrumbs.present` = true |
| 7 | Flexibility and efficiency of use | 2 | `home:skip_link.present` = false; `home:search.search_input` = true; `home:http.response_ms` = 1887; `home:scripts.external` = 18; `home:meta_viewport` = "width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" |
| 8 | Aesthetic and minimalist design | not judged | not judged from HTML: whether the page is crowded is a visual question; the HTML gives only counts such as `home:navigation.landmarks.0.links` = 63 and `home:visible_word_count` = 706. |
| 9 | Help users recognise, diagnose and recover from errors | not judged | not judged from HTML: no error messages or failed states appear on the page that could be read. |
| 10 | Help and documentation | 1 | `home:help_faq_contact_links.0` = "Contact us"; `home:footer_contact.phone_pattern` = true; `home:footer_contact.postal_address_pattern` = true; `home:footer_contact.email_pattern` = false |

Severity: 0 no problem, 1 cosmetic, 2 minor, 3 major, 4 severe (see HEURISTICS.md). Lower is better.

## Three suggestions for the web team
1. **Page structure of the home page · Consistency and standards.** Add one `h1`, a `main` landmark and a `lang` attribute on the `html` tag, and give the 3 images without `alt` text and the 25 links without text an accessible name. These are web standards that help screen readers.
2. **Zoom setting in the viewport tag · Flexibility and efficiency of use.** Remove `maximum-scale=1.0, user-scalable=no` so visitors who need larger text can zoom. Also add a "Skip to main content" link before the menu.
3. **The text field with a placeholder only · Error prevention.** Add a label to the field. Also replace the three "learn more" links with text that says what each leads to (Recognition rather than recall).

## Since last week
First audit; nothing to compare yet.

## Limits
Judged from the HTML of two pages only. Visual design, colour contrast and real tasks were not judged.
These findings are prompts for a human evaluator, not verdicts.

Only the home page could be read: the admissions page answered with a bot-check page (`admissions:outcome` = "bot_check_page"), which the audit did not try to get past. Findings rest on the home page.
