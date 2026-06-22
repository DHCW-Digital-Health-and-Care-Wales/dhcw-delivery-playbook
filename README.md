# DHCW Delivery Playbook

The source for the DHCW Product and Service Delivery Playbook, published as a website.

The content lives as Markdown in `docs/`. The site is built with [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) and published to GitHub Pages automatically on every push to `main`.

## Read it online

Once published, the site is at `https://dhcw-digital-health-and-care-wales.github.io/dhcw-delivery-playbook/`.

## Run it locally

You need Python 3.10 or newer.

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open `http://127.0.0.1:8000`. The site rebuilds as you edit any file in `docs/`.

## Make a change

1. Edit or add a Markdown file in `docs/`.
2. If you add a new page, list it in the `nav:` section of `mkdocs.yml`.
3. Commit and push to `main`. The site rebuilds and republishes within a minute or two.

Every page on the site has an "Edit this page" pencil that takes you straight to the right file on GitHub, so small fixes can be made in the browser.

## A note on tooling

The same Markdown content can also be built with [Zensical](https://zensical.org), the actively developed successor to Material for MkDocs from the same team. Zensical reads this `mkdocs.yml` natively, so moving across is a small change when you choose to.

## Contributing

This is a living document. Raise an issue or open a pull request. Contributions via your Delivery Manager are welcome.

---

Digital Health and Care Wales &bull; Iechyd a Gofal Digidol Cymru
