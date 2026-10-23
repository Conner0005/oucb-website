# oucb.uk

Website of the Oxford University Chemistry & Biochemistry Society (OUCB), hosted on GitHub Pages.

## Editing the site

You can edit everything on github.com: open a file, click the pencil icon, make the change, then **Commit changes**. The live site updates within a minute or two.

Most updates happen in the `CONFIG` and `SPONSORS` blocks near the bottom of `index.html`:

| Setting | What it does |
| --- | --- |
| `membershipFormUrl` | Link used by every "Buy membership" / "Join" button |
| `membershipFormEmbedUrl` | Full `docs.google.com/forms/…/viewform` link of the same form, shown on the page. `""` hides it |
| `membershipPrice` | e.g. `"£15"`. Leave `""` to hide |
| `academicYear`, `heroEyebrow` | Year shown on the membership card and the line above the main heading |
| `email`, `sponsorshipEmail` | Contact addresses |
| `instagram`, `facebook`, `x`, `linkedin` | Social links in the footer. Leave `""` to hide |
| `mailingListEndpoint` | Where mailing list sign-ups are sent (FormSubmit) |

### Sponsors

Add a line to `SPONSORS` in `index.html`:

```js
{ name: "Example Ltd", tier: "partner", logo: "assets/sponsors/example.png", url: "https://example.com" },
```

Upload the logo to `assets/sponsors/` first. `tier` is `"headline"` or `"partner"`. A sponsor page can live at `sponsorship/<name>/index.html`; copy `sponsorship/tpp/index.html` as a starting point.

### Committee

Edit `committee/index.html`. Each member is one `<li>` block: copy one, then change the name, role, college and subject. The tile shows two initials (e.g. `Ak`) and is coloured by subject: `tile chem` or `tile bio`.

## Mailing list

Sign-ups are emailed to ouchemsoc@gmail.com through [FormSubmit](https://formsubmit.co). The first submission from a new address triggers an activation email from FormSubmit; click its link once, or sign-ups won't be delivered.

## Files

- `index.html`: the homepage
- `committee/`: committee page
- `sponsorship/tpp/`: TPP sponsor page
- `assets/sponsors/`: sponsor logos and banners
- `Home/`, `events/`, `join-the-mailing-list/`, `sponsorship/`, `become-a-member/`: redirects from the old site's addresses to the matching section of the homepage
- `404.html`: page shown for addresses that don't exist

## Domain

The domain is registered at Namecheap. DNS for GitHub Pages:

| Type | Host | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `<github-account>.github.io` |

Leave the MX and `mail` records as they are.
