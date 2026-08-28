# Site edits — summary

All changes made to bring the site in line with the finalized CV. Nothing was deleted
that couldn't be re-enabled; demo pages were hidden from nav, not removed.

## CV page (/cv/)
- `assets/pdf/Shubham_Mirg_CV.pdf` — added (your compiled CV).
- `_pages/cv.md` — PDF button now points at Shubham_Mirg_CV.pdf; placeholder description replaced.
- `assets/json/resume.json` — FULL rewrite (this is the file that drives the CV page, not _data/cv.yml):
  - Added Google Scholar + ORCID to basics.profiles.
  - Work: T32 end-dated, teaching dates updated (incl. Spring 2026 BME 403).
  - Education: removed "Expected completion" note (you've graduated).
  - Skills: replaced old list (C, C++, Xilinx) with real groups — Pre-clinical & Imaging,
    Hardware, Software & Analysis — matching the CV.
  - Publications: added the two 2026 papers (bioRxiv "In Review" + npj Acoustics) and
    marked co-first-author papers.
  - Projects: added the trimodal fUS+optical project; changed all "Present" end dates to
    real end years; updated the multi-parametric entry to ULM/GBM.

## About page (/)
- `_pages/about.md` — fixed "Enginnering" -> "Engineering", "multimolal" -> "multimodal",
  "work also include" -> "work also includes" (+ minor grammar).

## Publications page (/publications/)
- `_bibliography/papers.bib` — replaced ALL Einstein placeholder entries with your 10 real
  papers. Your name is bolded via the scholar setting below.
- `_config.yml` — scholar last_name/first_name set to Mirg/Shubham (was Einstein/Albert)
  so your name is emphasized in the bibliography.

## Projects page (/projects/)
- `_projects/1-5_project.md` — replaced the 9 al-folio demo projects with 5 real ones
  (categories: "current" and "past").
- `_pages/projects.md` — display_categories updated to [current, past].

## Site identity
- `_data/socials.yml` — email set to smirg@psu.edu, Google Scholar ID set to your real one
  (uZLkn-kAAAAJ; was a placeholder), ORCID enabled (0000-0003-1811-6047).

## Nav cleanup
- Hidden from nav (set nav: false, not deleted): people (Einstein demo), submenus (demo),
  repositories (Torvalds demo repos), teaching (placeholder text).
  Re-enable any by setting `nav: true` in its _pages/*.md file.

## THINGS FOR YOU TO DO / CHECK
1. Project images are PLACEHOLDERS (assets/img/1.jpg–5.jpg, the al-folio stock photos).
   Swap in your own figures by replacing the `img:` path in each _projects/N_project.md.
2. Publication DOIs/URLs: only the Advanced Science paper has a live DOI in the bib. Add
   DOIs/URLs to the other entries in _bibliography/papers.bib when you have them.
3. Verify the two 2026 papers' status — bioRxiv is marked "In Review"; npj Acoustics is
   listed as published. Correct if either has changed.
4. This was NOT built with Jekyll here (no Ruby in the environment). Before making live,
   either push to a branch and let GitHub Pages build a preview, or run locally:
   `bundle exec jekyll serve`. All JSON/YAML/front-matter was validated and parses cleanly.
5. Optional: your live site currently shows fewer nav items than the repo — you may have
   local edits not in this ZIP. Reconcile if needed.
