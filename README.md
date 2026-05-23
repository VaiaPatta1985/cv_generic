# What is this?

This is a LaTeX setup to programmatically create a CV (`cv.tex`) and cover letter (`letter.tex`) tailored to a specific position; originally made for personal use, until I decided to share it with the world. I have removed my personal data and keep making it more generic so it can be useful to more people.

All information pertaining to the position, such as the job posting URL and the job title, is included in `position_details.tex`. In that file, you can currently choose between two languages, Greek and English (though I plan to make it more general). Be warned, though, that the way you are expected to write Greek is more than a little strange (eg opening and closing quotation marks are given by `((` and `))` respectively). If writing in Greek, you **must** use `\en{text}` whenever `text` is written in the latin alphabet.

Define the general layout of the CV and cover letter in `cv.tex` and `letter.tex` respectively. Furthermore, for the CV, define how specific items appear in `cv_template.tex`, and you can use those definitions in `cv_content_language.tex`.

Files `cv_content_english.tex` / `cv_content_greek.tex` and `letter_content_english.tex` / `letter_content_greek.tex` are where you write the actual content. Use `\hide{text}` to hide `text`. Use `\inif{\condition1\condition2}{text}` to show `text` whenever at least one of a set of conditions is nonzero and hide it otherwise; define these conditions as any number in `position_details.tex`.

For the CV, included packages along with some definitions are found in `cv_packages_etc.tex`. Note that you can also use a bibliography-style section to include any journal papers you may have authored, as long as you include their bibtex references in `cv.bib`.
