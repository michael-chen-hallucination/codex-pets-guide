# Codex Pets Beginner Guide

**Language:** English | [中文](./README.zh-CN.md)

This repository helps you choose, download, save, and install your favorite pet from [Codex Pets](https://codex-pets.net/#/?sort=popular&kind=person) for your own Codex setup.

It is written for beginners: start from opening the website, pick a pet you like, download it, and install it in Codex.

## What This Repo Includes

- A step-by-step beginner guide
- A folder for downloaded pet packages
- A folder for extracted pet files
- A simple list for tracking your favorite pets
- A GitHub-friendly structure you can use as your personal Codex pet collection

## Step 1: Open Codex Pets

1. Open your browser.
2. Go to:

   ```text
   https://codex-pets.net/#/?sort=popular&kind=person
   ```

3. This link sorts pets by popularity and filters for `person` pets.
4. If the page does not load immediately, refresh the browser once.

Note: `codex-pets.net` usually does not require an account for browsing, previewing, or downloading pets. The login you may need is for GitHub or the Codex app.

## Step 2: Pick a Pet You Like

1. Scroll through the page and browse the available pets.
2. When you find one you like, open its card or detail page.
3. Preview its animations, such as:
   - Idle
   - Run Right
   - Run Left
   - Wave
   - Jump
   - Failed
   - Waiting
   - Run
   - Review
4. If you like the look and animations, continue to download it.

## Step 3: Download the Pet

1. On the pet detail page, click `Download` or `Free Download`.
2. Your browser will download a `.zip` file.
3. Keep the zip file somewhere safe. This repo includes a `downloads/` folder for that purpose.

Recommended naming:

```text
downloads/pet-name.zip
```

Example:

```text
downloads/dad-coder.zip
```

## Step 4: Extract the Pet

1. Double-click the `.zip` file to extract it.
2. The extracted folder usually contains files like:
   - `pet.json`
   - `spritesheet.webp` or `spritesheet.png`
   - `preview.webp` or `preview.png`
   - sometimes `validation.json` or `source-sheet.png`
3. Move the complete extracted folder into this repo's `pets/` directory.

Recommended structure:

```text
pets/
  dad-coder/
    pet.json
    spritesheet.webp
    preview.webp
```

## Step 5: Install the Pet in Codex

On macOS or Linux, custom Codex pets usually live here:

```text
~/.codex/pets/
```

If your pet folder is named `dad-coder`, the final path should look like this:

```text
~/.codex/pets/dad-coder/
  pet.json
  spritesheet.webp
```

Copy it with:

```bash
mkdir -p ~/.codex/pets
cp -R pets/dad-coder ~/.codex/pets/
```

Then open Codex:

1. Open the Codex app.
2. Go to `Settings`.
3. Open `Appearance`.
4. Find `Pets`.
5. Select the custom pet you installed.
6. In the Codex input box, type:

   ```text
   /pet
   ```

7. Your pet should appear. Type `/pet` again to hide it.

## Step 6: Track Your Favorites

Use [pets-list.md](./pets-list.md) to record the pets you like.

Useful fields to track:

- Pet name
- Type
- Download or detail URL
- Whether it has been downloaded
- Whether it has been installed
- Notes about why you like it

## Step 7: Push This Repo to GitHub

If you are not logged in to GitHub CLI yet, run:

```bash
gh auth login
```

Choose:

1. `GitHub.com`
2. `HTTPS`
3. `Login with a web browser`
4. Copy the one-time code from your terminal
5. Log in through the browser and authorize GitHub CLI

After login, run this inside the repo folder:

```bash
git init
git add .
git commit -m "Add Codex Pets beginner guide"
gh repo create codex-pets-guide --public --source=. --remote=origin --push
```

For a private repository, replace `--public` with:

```bash
--private
```

## FAQ

### Do I need to log in to codex-pets.net?

Usually no. You can browse, preview, and download directly from the website.

### Codex cannot find my pet. What should I check?

Check these three things:

1. The pet folder is under `~/.codex/pets/`.
2. The folder contains `pet.json`.
3. The folder contains `spritesheet.webp` or `spritesheet.png`.

### My pet does not show up. What should I do?

First, type this in Codex:

```text
/pet
```

Then check `Settings > Appearance > Pets` and make sure your custom pet is selected.

## Reference

- [Codex Pets popular person page](https://codex-pets.net/#/?sort=popular&kind=person)
