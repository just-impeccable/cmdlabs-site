# CMDLabs LLC Website

Static GitHub Pages site for CMDLabs LLC public app documents.

## Public URLs

When published with the custom domain, the intended URLs are:

- `https://cmdlabs.us/`
- `https://cmdlabs.us/privacy/`
- `https://cmdlabs.us/terms/`
- `https://cmdlabs.us/disclaimer/`
- `https://cmdlabs.us/support/`

## GitHub Pages Setup

1. Create a GitHub repository under the CMDLabs account, for example `cmdlabs-site`.
2. Push these files to the repository's `main` branch.
3. In GitHub, open the repository settings.
4. Go to `Pages`.
5. Set the source to deploy from `main` and `/root`.
6. Set the custom domain to `cmdlabs.us`.
7. Enable `Enforce HTTPS` after DNS has propagated and GitHub allows it.

## GoDaddy DNS

In GoDaddy DNS for `cmdlabs.us`, configure GitHub Pages records.

For the apex/root domain, add these `A` records:

```text
Host: @  Value: 185.199.108.153
Host: @  Value: 185.199.109.153
Host: @  Value: 185.199.110.153
Host: @  Value: 185.199.111.153
```

For `www`, add this `CNAME` record:

```text
Host: www  Value: <cmdlabs-github-username>.github.io
```

Replace `<cmdlabs-github-username>` with the exact GitHub username or organization name that owns the Pages repository.

DNS can take minutes to 24 hours to settle.
