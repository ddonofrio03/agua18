# agua18.com

Simple single-page site for AGUA18. Static HTML — works on GitHub Pages or any static host.

## Structure

```
index.html        # the whole site
assets/logo.png   # logo
```

## Activating the contact form

The form posts to [Formspree](https://formspree.io/). To turn it on:

1. Sign up at https://formspree.io (free tier is fine).
2. Create a new form, pick the destination email address.
3. Copy the form ID Formspree gives you (looks like `xpzgwabc`).
4. In `index.html`, find this line:
   ```html
   <form class="contact" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   Replace `YOUR_FORM_ID` with your actual ID.
5. Commit and push. The next form submission will arrive in your inbox.

Until you do that, the form will look right but submissions will 404.

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```
python3 -m http.server 8000
```

then visit http://localhost:8000.

## Deploy (GitHub Pages)

In the repo settings → Pages → Source: `main` branch / `/ (root)`. The site will be served at `https://ddonofrio03.github.io/agua18/`.

To use the custom domain `agua18.com`, add a `CNAME` file at the repo root containing `agua18.com` and point your domain's DNS to GitHub Pages.
