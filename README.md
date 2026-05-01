### Michael R. Berthold – Jekyll Site

Jekyll site for GitHub Pages.

---

## Setup

1. Extract the project files locally  
2. Upload all files **directly to the repository root**  
   (do not upload the ZIP and do not place them into an `mb` subfolder — keep the folder structure as-is)  
3. Update `_config.yml`:

```yaml
url: "https://michael-berthold.github.io"
baseurl: ""
````

4. Push to the `main` branch and enable GitHub Pages (Settings → Pages)

The site will be available at:
[https://michael-berthold.github.io/](https://michael-berthold.github.io/)

---

## Structure

* `_layouts/` → page templates
* `_includes/` → reusable components (header, footer)
* `assets/` → images, video files and styles
* `_books/` → books shown on the homepage
* `_publications/` → publications / articles
* `_musings/` → blog posts with their own pages
* `_videos/` → video content
* `_data/` → structured data used across the site

  * `site_settings.yml` → global contact details (used in the footer across the site)
  * `contact_page.yml` → contact page specific content (press contact, social links, texts)
  * `peer_reviewed_publications.yml` → list of peer-reviewed publications
  * `edited_volumes.yml` → list of edited volumes
* `de/` → German homepage
* `_config.yml` → main site configuration (site URL, baseurl, collections, defaults, permalinks)

---

## Content editing

### Publications

Go to the `_publications/` folder and open an existing file.
Copy it, rename it, and update the fields with the new content.

Publication files currently do **not** generate their own pages (`output: false` in `_config.yml`).
They are used as structured content for listings.

If needed, they can be extended with body content and turned into full pages by setting:

```yaml
collections:
  publications:
    output: true
```

---

### Books

Go to the `_books/` folder and update or copy an existing file with new data.

Book files also do **not** generate their own pages by default.
They are used for homepage cards.

They can be extended and turned into pages by enabling output in `_config.yml`.

---

### Musings (blog posts)

Go to the `_musings/` folder and update or copy an existing file.

These automatically generate their own pages.

---

### Peer-reviewed publications

Edit `_data/peer_reviewed_publications.yml` to update the peer-reviewed publications list.

---

### Edited volumes

Edit `_data/edited_volumes.yml` to update the edited volumes list.

---

### Videos

Go to the `_videos/` folder and update or copy an existing file.

The video files are not uploaded yet. They need to be added to the `assets/img/videos/` folder, 
and then their file paths should be inserted into the appropriate file in the `_videos` directory.


---

### Contact data

* Edit `_data/site_settings.yml` to update global contact details (used in the footer)
* Edit `_data/contact_page.yml` to update the contact page content

---

### Site configuration

Edit `_config.yml` to update core site settings such as:

* site title and description
* site URL and baseurl
* collection behavior
* default layouts and language settings

---

Always copy an existing file to keep the correct structure.

