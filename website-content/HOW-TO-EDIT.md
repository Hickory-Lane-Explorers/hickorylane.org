# How to change the website

All words and pictures of the website are in this folder. You do not need to touch other folders.

| File | What it controls |
| --- | --- |
| `home-page.yaml` | The Home page |
| `organization-page.yaml` | The Our Organization page |
| `board-page.yaml` | The Our Board page |
| `every-page.yaml` | The site name, the banner photograph, and the footer on all pages |
| `appearance.yaml` | The colors and fonts of all pages |

## The easy way: the web editor

Open https://app.pagescms.org and sign in with the link from your invitation email. Select a page on the left, change the text in the form, and press **Save**. The website updates by itself a few minutes later.

To change a photograph, click the photograph field and upload a new picture. The website makes the picture the correct size.

## The direct way: change the text files

Open a file in a plain text editor. Each line has a label, then a colon, then the text:

```yaml
heading: After-School Program
```

Change only the text after the colon. Obey these four rules:

1. Do not change the labels on the left of the colon.
2. Do not change the spaces at the start of a line. The spaces show which lines are together.
3. If your text contains a colon followed by a space, or starts with `*`, `"`, `&`, or a number with a zero in front (`03`), put the text in double quotes: `footnote: "*Dates may change"`.
4. Long text starts with `|` on the label line. Put the text on the lines below, all with the same spaces in front. Leave an empty line between paragraphs.

In long text, put two stars on each side of words to make them bold: `**Discover the joy**`.

### Add an item to a list

A list item starts with a dash. To add a date, copy a full item and change it:

```yaml
    - date: Nov. 19
      topic: Capstone Presentation
    - date: Dec. 03
      topic: Your new topic
```

### Change the dates calendar

The website draws the calendar from the `dates` part of `home-page.yaml`:

```yaml
dates:
  heading: Dates
  start_year: 2026
  months:
    - month: September
      days: 03, 10, 17, 24
```

Write the year of the first month after `start_year:`. The website adds the years to the heading and moves to the next year after December. Write the full month name. Write each day with two digits. If a month name or a date is not possible, the website does not update until you correct it.

### Add a board member

Copy a full member in `board-page.yaml`, from the line `- name:` to the end of the biography. Then change the text. Put the photograph file in `static/images/photographs/` and write its name after `photograph:`, for example `/images/photographs/anna-vilinskiy.jpg`. If `photograph:` has `""`, the website shows a leaf picture.
