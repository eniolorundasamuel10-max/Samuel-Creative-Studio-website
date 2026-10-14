# Samuel Creative Studio: Portfolio Website

A fast, responsive portfolio website for Eniolorunda Samuel. It uses plain HTML, CSS and JavaScript, so there is nothing to install and no build step. You can open `index.html` in any browser to preview it.

## What is in this folder

```
samuel-creative-studio/
├── index.html              ← all the page text and sections
├── css/styles.css          ← colours, fonts and layout
├── js/
│   ├── config.js           ← contact form setup
│   ├── portfolio-data.js   ← your portfolio projects
│   └── main.js             ← menu, gallery and form behaviour (no need to edit)
└── assets/
    ├── favicon.svg         ← browser tab icon
    └── images/             ← portfolio images (samples for now)
```

## 1. Editing text

Open `index.html` in a text editor (VS Code is free and works well). Sections are marked with comments such as `<!-- ============ SERVICES ============ -->`. Change the words between the tags, for example:

```html
<h3>Flyer and Poster Design</h3>
<p>Change this sentence to change the description.</p>
```

Do not delete the `<` and `>` symbols or the tag names. Save the file and refresh your browser to see the change.

## 2. Changing colours and fonts

Open `css/styles.css`. The first block, `:root { ... }`, holds every colour:

| Name | What it controls |
|------|------------------|
| `--bg` | main dark background |
| `--violet` | button colour |
| `--violet-2` | light purple highlights |
| `--pink` | gradient partner colour |
| `--text` | main text colour |

Change a value such as `--violet: #7c3aed;` and the whole site updates.

## 3. Replacing the sample portfolio with your real work

Every project in the gallery is a sample concept and is labelled as one on the site. To replace one:

1. Save your image into `assets/images/` (JPG, PNG or WebP). Keep it under about 300 KB. You can shrink images for free at https://squoosh.app.
2. Open `js/portfolio-data.js`.
3. For the project you are replacing, change `image`, `title`, `alt` (a short description for screen readers), `category` and `description`.
4. Change `sample: true` to `sample: false`. This removes the "Sample concept" label.

To add a project, copy one `{ ... }` block, add a comma after the previous block and edit it. To delete a project, remove its block. The `category` must match one of the names in the `categories` list at the top of that file.

**Your photo:** in `index.html`, find the comment that begins "To use a real photo" in the About section and follow it.

## 4. Making the contact form work

The Email Me and Chat on WhatsApp buttons work now. The form needs a free service to deliver messages to your inbox, because a website alone cannot send email.

1. Create a free account at https://formspree.io.
2. Create a new form and set your email, `eniolorundasamuel10@gmail.com`, as the destination.
3. Copy the form URL (it looks like `https://formspree.io/f/abcdwxyz`).
4. Open `js/config.js` and paste it between the quotes of `formEndpoint: ""`.
5. Save and publish again (see below). Send yourself a test message.

Until you do this, the form does not pretend to send. It tells the visitor that nothing was sent and gives them a WhatsApp and email link instead.

## 5. Saving your files on GitHub (free)

1. Create a free account at https://github.com.
2. Click **New repository**, name it `samuel-creative-studio`, choose **Public**, and click **Create repository**.
3. Click **uploading an existing file**, drag in everything inside this folder (keep the `css`, `js` and `assets` folders), and click **Commit changes**.

Important: `index.html` must be at the top level of the repository, not inside another folder.

## 6. Publishing to a live URL (GitHub Pages, free, no domain needed)

1. In your repository, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose branch **main** and folder **/ (root)**, then click **Save**.
4. Wait one to two minutes and refresh. Your site appears at:
   `https://YOUR-GITHUB-USERNAME.github.io/samuel-creative-studio/`

You do not need to buy a domain. You can add one later under the same Pages settings.

## 7. Updating the live site after changes

1. On GitHub, open the file you want to change and click the pencil icon (Edit), or choose **Add file → Upload files** to add new images.
2. Make your change and click **Commit changes**.
3. Wait one to two minutes, then refresh your live site. Press Ctrl + F5 (Cmd + Shift + R on Mac) if you still see the old version.

## Before you go live: checklist

- [ ] Replace sample projects, or leave the "Sample concept" labels in place.
- [ ] Connect the contact form (section 4) and send a test message.
- [ ] Add your photo if you want one.
- [ ] Open the live link on your phone and click every button.

## Good to know

- The site loads two fonts (Inter and Sora) from Google Fonts. If they cannot load, it falls back to your device's standard fonts and stays readable.
- No client names, testimonials or awards are included. Add them only when they are real.
