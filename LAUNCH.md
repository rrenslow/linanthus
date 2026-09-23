# Publish Linanthus Labs

Selected setup: **GitHub Pages for hosting + GoDaddy for the domain and DNS**. The contact email is **linanthuslabs@gmail.com**, which the owner has created. No website hosting purchase or nameserver change is needed.

The package is ready to upload. It has not been published by the assistant. The connected GitHub integration reports read access, without repository write or administration access.

## 1. Upload the website

1. Unzip `Linanthus_Labs_Website.zip` and open the extracted `linanthus` folder.
2. Open [the repository](https://github.com/rrenslow/linanthus). For an empty repository, click **uploading an existing file**. For a populated repository, choose **Add file → Upload files**.
3. Drag in the **contents** of the extracted `linanthus` folder, including the `docs` folder, `brand-assets`, and the Markdown guides. Do not upload the ZIP or add another enclosing `linanthus` directory.
4. Commit to `main` with the message `Add Linanthus Labs website`.

**Checkpoint:** the repository contains `docs/index.html`, `docs/styles.css`, and `docs/assets/` at those exact paths.

## 2. Enable GitHub Pages

Open [Settings → Pages](https://github.com/rrenslow/linanthus/settings/pages). Under **Build and deployment**, select:

| Setting | Value |
| --- | --- |
| Source | Deploy from a branch |
| Branch | main |
| Folder | /docs |

Click **Save**. No custom workflow or build command is required. Changes committed to `docs/` on `main` will be published automatically. The package includes a `CNAME` file, but you must still set the custom domain in the Pages settings below.

Source: [GitHub publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## 3. Connect linanthus.com

Before changing the website's DNS records, verify the domain and add it to this repository:

1. Open your [GitHub account's Pages settings](https://github.com/settings/pages), choose **Add a domain**, and enter `linanthus.com`. Add the exact TXT record GitHub supplies in GoDaddy's DNS editor, then click **Verify** in GitHub. Keep that TXT record after verification.
2. Return to the [repository's Pages settings](https://github.com/rrenslow/linanthus/settings/pages). Enter **linanthus.com** under **Custom domain**, then click **Save**. The DNS check may initially fail until the next step is complete.
3. In GoDaddy, open **My Products → linanthus.com → DNS**. Keep GoDaddy's nameservers. Set the following website records, using the default TTL:

| Type | Name | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | rrenslow.github.io |

Replace conflicting parking or website A records for `@` and any conflicting `www` record. Remove or correct stale AAAA records pointing to a different website host. Preserve unrelated TXT, MX, NS, and other service records. The `www` target is **rrenslow.github.io**, with no protocol or repository name. Do not configure GoDaddy domain forwarding for this connection.

4. Wait for the GitHub DNS check and certificate to succeed, then select **Enforce HTTPS**. DNS and certificate provisioning can take up to 24 hours.
5. Open `https://linanthus.com` and `https://www.linanthus.com`. Both should reach this site, with `www` redirecting to the apex domain.

**Checkpoint:** both addresses load securely, and **Email Linanthus Labs** opens a message to `linanthuslabs@gmail.com`.

Sources: [GitHub custom domains and DNS](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site), [Domain verification](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages).

## 4. Forward business email to the main inbox

The website already uses `mailto:linanthuslabs@gmail.com`. No domain email purchase or MX change is needed for this Gmail address.

1. In **linanthuslabs@gmail.com**, open **Settings → See all settings → Forwarding and POP/IMAP → Add a forwarding address**.
2. Enter your main Gmail address with a business tag, such as `PRIMARYUSERNAME+linanthus@gmail.com`, replacing `PRIMARYUSERNAME` with your actual username. The tagged address delivers to the existing main inbox.
3. Confirm the verification message in the main inbox. Return to the business account, enable forwarding, and save.
4. In the main inbox, create a filter with `deliveredto:PRIMARYUSERNAME+linanthus@gmail.com` in **Has the words**, and apply the label **Linanthus Labs**.
5. To reply from the business address, use the main account's **Settings → Accounts and Import → Send mail as → Add another email address**. Add **Linanthus Labs / linanthuslabs@gmail.com**, complete verification, and select that address in the **From** field when replying or composing business mail.
6. Send a test from an unrelated account, check the label, and test a reply.

Gmail does not forward messages classified as spam. Check the source account's spam folder, account notices, and storage periodically. Keep two-step verification and recovery methods enabled.

Sources: [Gmail forwarding](https://support.google.com/mail/answer/10957), [Send mail as](https://support.google.com/mail/answer/22370), [Search operators](https://support.google.com/mail/answer/7190).

## GitHub Pages policy

This package is an informational consulting website with email contact links. GitHub's published terms restrict using Pages to run an online business or primarily facilitate commercial transactions. They do not expressly exempt every consulting brochure site merely because it has no checkout. The owner has chosen this setup with that uncertainty understood; this guide does not represent GitHub's approval. The static files remain portable if a different host is needed later.

Source: [GitHub Pages terms](https://docs.github.com/en/site-policy/github-terms/github-terms-for-additional-products-and-features#pages).

Instructions checked against official documentation on September 23, 2026.
