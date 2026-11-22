# Your website guide

This note is for you, Katie. It explains what this project is, how the website goes live, and how to change it after the project moves to your GitHub account.

## What this is

This repository is the project folder on GitHub that holds your public biography page. It is a simple website: one main page, a stylesheet, your resume, and a few small images. There is no app to install and no separate publishing program.

The page introduces you as a Clinical Research Specialist in Carolina Beach, NC. The words on the page come from your resume. The page does not add employers, dates, or credentials that are not already in that resume.

- Your project on GitHub: https://github.com/katievbuck/Katie-Buck-Bio
- Your public website, after the move: https://katievbuck.github.io/Katie-Buck-Bio/

You own the project once you accept the transfer. The repository name stays `Katie-Buck-Bio`.

## How the website gets published

GitHub publishes the site for you. You do not upload the page to a separate web host.

A file named `.github/workflows/pages.yml` runs every time a change is saved on the `main` branch. GitHub calls that automation an Action. In the Actions tab its name is **Deploy Katie Buck bio to GitHub Pages**. When that run finishes with a green check, the public page updates. That usually takes a minute or two.

You can also start it yourself:

1. Open the project on GitHub.
2. Click the **Actions** tab.
3. Click **Deploy Katie Buck bio to GitHub Pages**.
4. Click **Run workflow**, leave the branch set to `main`, and confirm.

## How to accept the transfer

The project is moving from the GitHub account `willyd61` to your account, `katievbuck`. GitHub does not finish that move until you accept it.

1. Sign in to GitHub as **katievbuck** at https://github.com/katievbuck.
2. Watch the inbox for the primary email address on that GitHub account. GitHub sends a message that a repository transfer is waiting. The message includes a link and instructions for accepting the transfer.
3. Open that email and follow the link.
4. Read the confirmation page and accept the transfer.

Accept it within one day. After that, the invitation expires and it has to be sent again. If the email does not arrive, check spam, and confirm that the primary email on your GitHub account is one you can open. GitHub sends the invitation to that address.

When the transfer finishes, the project is at https://github.com/katievbuck/Katie-Buck-Bio.

## Checklist after the transfer

Do this once on the new project.

1. **Set the publishing source.** Open the project, click **Settings**, then **Pages**. Under **Build and deployment**, set **Source** to **GitHub Actions**. Until this is set, saving a change will not update the public page.

2. **Turn on HTTPS.** On that same Pages screen, check **Enforce HTTPS** so visitors use the secure address (the one that starts with `https://`). If the box is unavailable, wait a few minutes and look again. GitHub needs a moment to prepare the certificate.

3. **Enable Actions if GitHub asks.** Open the **Actions** tab. If you see a button to enable workflows, click it. If the public page is not up yet, open **Deploy Katie Buck bio to GitHub Pages** and use **Run workflow** once.

4. **Set the description and website.** On the main project page, click the gear icon next to **About**.
   - Description: `Professional bio for Katie Buck, Clinical Research Specialist.`
   - Website: `https://katievbuck.github.io/Katie-Buck-Bio/`
   - Save the changes.

5. **Confirm the new site loads.** Open https://katievbuck.github.io/Katie-Buck-Bio/ and check that your name and the page sections appear. A private or incognito window avoids an old saved copy. If you see a “404” page, return to steps 1 and 3 and wait for the Action to finish with a green check.

6. **The old address stops working.** The previous public address, https://willyd61.github.io/Katie-Buck-Bio/, will stop working. GitHub does not forward that old Pages address to your new one. Share https://katievbuck.github.io/Katie-Buck-Bio/ from here on.

## How to edit the words on the page

The visible text lives in a file named `index.html`. You can change it in the browser.

1. Open https://github.com/katievbuck/Katie-Buck-Bio.
2. Click `index.html`.
3. Click the pencil icon (**Edit this file**). Sign in if GitHub asks.
4. Change the sentences you want to change. Leave the words inside angle brackets (`<` and `>`) as they are unless you are updating a link on purpose.
5. Click **Commit changes**.
6. Choose **Commit directly to the `main` branch**.
7. Write a short note, such as `Update experience summary`, and confirm.

GitHub then runs the publishing Action. Refresh the public site after a minute or two.

If a change does not look right, open `index.html` again and use **History** on that file. GitHub keeps earlier versions, and you can restore one.

## How to replace your resume

The page offers two downloads in the `assets` folder:

- `Katie-Buck-Resume.pdf`
- `Katie-Buck-Resume.docx`

Keep those exact file names and the buttons keep working. If you choose a different name, update the links as described below.

Before you upload a new resume, open it on your computer and remove any phone number and any street address. Those do not belong in this public project. The city and state already shown on the page can stay. Do not type a phone number or a home street address into `index.html` or any other file here.

To replace a file on GitHub:

1. Open the `assets` folder.
2. Click the resume file you are replacing.
3. Click the trash icon, then commit that deletion to the `main` branch.
4. Click **Add file**, then **Upload files**, and choose the new PDF or Word file.
5. Check that the uploaded name is exactly `Katie-Buck-Resume.pdf` or `Katie-Buck-Resume.docx`.
6. Commit the upload directly to the `main` branch.

If the new file has a different name, upload it and then edit `index.html`. Search for `Katie-Buck-Resume` and point each resume link at the new name. There are download buttons near the top of the page and again in the Contact section. Near the top of `index.html` there is also a block that starts with `application/ld+json`. That block lists the two resume web addresses. Update those two addresses as well, using `https://katievbuck.github.io/Katie-Buck-Bio/assets/` plus the new file name.

The buttons also show a file size, such as “73 KB”. If the new file is a different size, change that number in the button text so it stays accurate.

## How to update the preview image

When someone shares your site, a preview card can appear in the message. That picture is `assets/og-image.png`. The page describes it as 1200 pixels wide by 630 pixels tall. The current card is text only.

Replace it the same way as the resume: delete `og-image.png` in `assets`, then upload the new picture with the same name, `og-image.png`. The links in `index.html` already point at that name, so you do not edit them if the name stays the same.

If you give the picture a new name, update every `og-image.png` address in `index.html` to the new name. Those addresses use the full site URL, `https://katievbuck.github.io/Katie-Buck-Bio/assets/`, followed by the file name.

Preview images are often saved by the app that shows them. A new picture can take a while to appear in LinkedIn, Messages, or similar apps even after your site has updated.

## Optional: use your own web address

You can keep the free address https://katievbuck.github.io/Katie-Buck-Bio/. You do not need to buy a domain.

If you later want an address you own:

1. Open **Settings**, then **Pages**.
2. Under **Custom domain**, type the domain and save.
3. At the company where you bought the domain, add the DNS records GitHub shows on that Pages screen. GitHub’s guide walks through the records: [Configuring a custom domain for your GitHub Pages site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
4. When GitHub says the domain is ready, check **Enforce HTTPS**.
5. Update the address written inside the project so search engines and link previews use the new domain. In `index.html`, `sitemap.xml`, and `robots.txt`, replace `https://katievbuck.github.io/Katie-Buck-Bio/` with your domain, including the preview-image links. Ask for help with that edit if you would rather not change those files yourself.

This site is published by the Action in `.github/workflows/pages.yml`, so the domain is set under **Settings → Pages**. You do not add a separate `CNAME` file for that.

## How to get help

- This guide is the short version. [README.md](../README.md) has more detail about the files.
- GitHub’s instructions:
  - [Transferring a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/transferring-a-repository) — the email GitHub sends you is the step that completes the move.
  - [About GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)
  - [Editing files](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files)
  - [Securing your GitHub Pages site with HTTPS](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)
- After a transfer between personal accounts, GitHub keeps the previous owner as a collaborator. On this project that account is [willyd61](https://github.com/willyd61). You can ask there if a publishing step fails.
- GitHub Support: https://support.github.com/
