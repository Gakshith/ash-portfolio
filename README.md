# ash-portfolio

Akshith Gojuru's portfolio: an AI/ML engineer and Computer Science student at San Francisco State.
The site is set in a night-time city. Bats form the name in the hero, and a rooftop searchlight lights up the contact section.

Live: https://akshith-gojuru.vercel.app

## Run it

The whole site is one static `index.html`. It has no build step and no dependencies.

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

## Deploy

The site is hosted on Vercel as a static site. `vercel.json` sets clean URLs and a few headers.

```bash
npx vercel          # preview
npx vercel --prod   # production
```

## Contact form

The form posts to FormSubmit (`CF_ENDPOINT` in `index.html`). The first message sent triggers a
one-time activation email to the inbox. If the post fails, the form opens the visitor's email app instead.
