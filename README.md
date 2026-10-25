# Souvick Bera — academic website

This is a six-page static HTML/CSS template for GitHub Pages. The design takes
inspiration from the minimal academic presentation of Hugo Barks; it is original
HTML/CSS, not an installation of the Barks Hugo theme. No Hugo, JavaScript,
package installation, or build step is needed.

## Pages

| File | Contents |
| --- | --- |
| index.html | Bio only; the default landing page |
| research.html | Research introduction, working papers, submitted or accepted papers |
| teaching.html | Institution headings and course lists |
| cv.html | Curriculum Vitae |
| news.html | Poster, talk, and paper acceptance examples, in that order |
| contact.html | Contact details |
| assets/style.css | Shared typography, colors, layout, and responsive styles |
| images/ | Six original decorative SVG banners |
| favicon.png | Replaceable sample icon; overwrite it with your own PNG logo |

## Use the template

1. Extract the ZIP. Open index.html in your browser to preview it. All navigation
   and local assets also work when previewed directly from your computer.
2. Review each HTML file and replace the bracketed placeholders with your actual
   details. Existing page contents were not supplied in full, so this is a starter
   based on the snippets and research description in the conversation.
3. Copy your existing detailed content into the relevant page, below its banner.
   Keep only the Bio section in index.html. Each other page contains only its own
   category. Do not paste all sections back into index.html.
4. Upload the extracted files AND the assets/ and images/ folders into the folder
   your existing GitHub Pages site publishes. Keep all six HTML files together.
   If your source is the repository root, put index.html there, not inside an
   additional souvick-academic-site/ folder. If your source is /docs, use /docs.
   Upload the contents of the ZIP rather than only the ZIP file.
5. For a branch-based Pages site, GitHub Settings > Pages > Build and deployment
   can use 'Deploy from a branch', your source branch, and '/(root)' or '/docs'.
   Keep an existing working Pages setup if you already have one.

## Why these are separate pages

The menu uses research.html, teaching.html, cv.html, news.html, and contact.html.
It does not use #research or other same-page section links. Clicking the name
returns to index.html. The current menu item has aria-current="page" and a sand
underline. Relative paths support both username.github.io and project sites.

Headers and footers are copied in each HTML file to avoid a build dependency.
When changing shared menu text or social URLs, edit all six copies. For example,
you may change the visible CV menu label to Curriculum Vitae in every header.

## Replace a banner with your photograph

Upload a photo, for example images/research-background.jpg. In research.html,
change the banner image src from images/research-background.svg to that filename.
Each page can use a different picture. Use a reasonably wide photograph.
The title is centered over the banner, with all writing below it.

Use .section-banner img { object-position: center 35%; } in the shared CSS to
adjust the crop. Banner height is 210px on desktop and 160px on small screens.
To darken photo banners more, increase the alpha in .section-banner::after.

## Profile photo

The profile image in index.html is intentionally commented out. Upload your
photo as images/your-photo.jpg and remove only the comment markers around its
img element when ready. It appears to the left of the Bio text on wide screens,
and above the text on small screens. No empty photo column is shown while hidden.

## Colors and headings

Edit the :root variables at the top of assets/style.css:

- Slate blue: #5b5f97 (subsection headings)
- Dark slate blue: #42466f (links and name)
- Warm ivory: #faf8f3 (page background)
- Sand: #b49a75 (active menu accent)

All h2, h3, and h4 subsection headings are slate blue, including those in Bio.
The main page title is white over the banner. Paper titles are regular weight,
not italicized, and not linked. DOI or arXiv links can be added below each title.

## Details to complete before publishing

- Add your current position/institution and any collaborator links in index.html.
- Replace paper titles, authors, descriptions, and publication status in research.html.
  Do not leave the example placeholders as publication claims.
- Check the course details and replace the institution heading in teaching.html.
- Add your actual cv.pdf alongside cv.html. Uncomment its download link, and
  replace the availability sentence. No placeholder PDF is supplied.
- Replace the dates, titles, journal, and conference names in news.html. Keep the
  most recent item at the top; the ordering is manual, not automatically sorted.
- Add your contact details in contact.html.
- All four social icons are visible in the footer of every page: Outlook-style
  email, LinkedIn, Google Scholar, and GitHub. They are inline SVGs, so they do
  not need an icon font, CDN, JavaScript, or a network request. Replace YOUR_EMAIL,
  YOUR_USERNAME, and YOUR_ID in each page's footer with your real destinations.
  The email link uses mailto:, which opens the visitor's configured mail app;
  the Outlook-style icon does not force the use of Outlook.
  These links are placeholders until you edit them; no profile URL was guessed.

## References

- Barks: https://github.com/timothygebhard/barks
- GitHub Pages publishing sources:
  https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- Google's favicon guidelines:
  https://developers.google.com/search/docs/appearance/favicon-in-search

## Favicon in Google results

All pages, including index.html, contain this line in their head:

    <link rel="icon" type="image/png" href="favicon.png">

Upload your own logo as favicon.png alongside index.html. Overwrite the sample
SB PNG included in this package. Use a square image, preferably 96 by 96 pixels
or larger, with a recognizable design at small sizes. No ICO conversion is
needed. If you choose a different filename, update the href on all six pages.
The HTML does not hardcode sizes, so it also supports a higher-resolution PNG.

After publication, Google must recrawl the home page and icon. This can take
days or weeks, and display is not guaranteed. If you use Google Search Console,
you can request indexing of the homepage through URL Inspection. Google uses
one favicon per hostname; separate project subdirectories on the same hostname
cannot set separate search-result favicons. Keep the files crawlable and their
URLs stable. The download package does not itself publish or index the site.

The actual Barks theme requires a Hugo project and Hugo Extended for its SCSS.
This plain-HTML template borrows its minimal academic direction, with no copied
theme code, fonts, or images.
