# Engineering portfolio

A lightweight, responsive portfolio using plain HTML and CSS. No dependency installation or build is required.

## Develop

Use the existing checkout; each Codex cloud task is already isolated. From `/workspace/Website`, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open the site in a local browser when working on your own machine. In cloud tasks, use local HTTP requests for validation; the onboarding UI does not provide a localhost preview.

## Personalize

- Edit `index.html` to add your name, discipline, interests, and real projects. Project cards and individual pages are labeled templates until you add real content.
- For each project, explain the problem, constraints, your role, design decisions, validation, and lessons learned. Add photographs with descriptive alt text.
- Replace the CV placeholder with an anchor to your PDF, for example `<a href="assets/cv.pdf">Download CV (PDF)</a>`, and add the PDF at that path. Do not add the link before the file exists.
- Keep a short background summary on the website and the detailed history in your CV.
- Add gingerbread photos in `assets/gingerbread/`, then replace the empty gallery figure in `index.html` with one figure per creation. Use a real image, descriptive alt text, and a caption. For example:

  ```html
  <figure class="gallery-photo">
    <img src="assets/gingerbread/house.jpg" alt="Describe your actual gingerbread house" loading="lazy" width="1200" height="900">
    <figcaption><strong>Your creation’s title</strong><span>Year · A short story about the build</span></figcaption>
  </figure>
  ```

  Use your photo’s actual dimensions. Photos are stored in Git; posting currently means adding files and updating the gallery through Codex or your editor.
- Edit `styles.css` for the design.

## Push and publish

Review changes, then commit and push from your local checkout or ask Codex to do so. This version is stored at the repository root; the earlier exported portfolio remains in `dist/`.

This site can be hosted by GitHub Pages: push the files to `main`, then in the repository's Pages settings select deployment from `main` and the repository root. The relative asset paths also work under a repository subpath. Publication has not been configured or verified.

For future iterations, ask Codex to edit the repository with a concrete request, such as adding a project case study or updating the CV link.

## Individual project pages

The homepage links to `projects/project-01.html`, `projects/project-02.html`, and `projects/gingerbread-01.html`. All share `styles.css` and work without JavaScript or a build step.

To add a project, copy a page in `projects/`, choose a descriptive filename, update its title, introduction, story, image alt text, and captions, and add a corresponding card in `index.html`. Remove the template labels once the content is real.

Put your photos in `assets/` (for example `assets/projects/my-project/`). On a project page, both the image `src` and its surrounding link `href` must use the same `../assets/...` path so visitors can open the full-size photo. Set each image’s actual width and height and describe its content in the alt text. Duplicate a `project-photo` figure to add more photos. Short captions appear below every image, and the first gallery photo spans both desktop columns. Galleries stack on mobile.

The current SVG images in `assets/placeholders/` are labeled placeholders, not project photographs. Replace them with your own images. The gingerbread homepage card can link to a new creation page using the same pattern.
