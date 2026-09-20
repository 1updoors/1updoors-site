# 1upDoors publishing preparation

Status: local draft with the original 1upEmblem.png included alongside index.html. The logo filename is case sensitive on GitHub Pages. Live publishing is still pending.

The header uses the original emblem without stretching or cropping, alongside the company name. All phone, text, email, service, and service-area content is preserved. Relative image paths work on both the current project URL and the custom domain.

## Check and publish the branding

1. Keep index.html and the included 1upEmblem.png together in the same directory.
2. Preview at desktop and mobile widths. The original white background is preserved inside a rounded white tile against the dark header. Browser visual verification is still pending.
3. Upload the reviewed index.html and 1upEmblem.png to the repository root. Keep Pages set to main / (root).
4. Wait for the Pages deployment and check https://1updoors.github.io/1updoors-site/. Confirm the logo loads and Call/Text buttons still use 248-309-9434.

## Connect 1updoors.com when ready to launch

1. Verify ownership through GitHub account Settings > Pages, using the TXT record GitHub supplies.
2. In repository Settings > Pages, set Custom domain to 1updoors.com and save before changing DNS. For this branch-based deployment GitHub creates the CNAME file.
3. At the domain's DNS provider, configure these records:

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | 1updoors.github.io |

Replace conflicting website records for these hosts as appropriate. Preserve email MX and email-related TXT records so service@1updoors.com is not disrupted. The www target must not include /1updoors-site/.

4. Allow DNS and certificate provisioning to finish (up to 24 hours), then enable Enforce HTTPS in Pages.
5. Confirm https://1updoors.com loads the logo, https://www.1updoors.com redirects correctly, and phone, text, email, and section links work on a phone.

The existing canonical URL and business structured data already target 1updoors.com. No domain settings or DNS records have been changed in this task.

Official reference: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
