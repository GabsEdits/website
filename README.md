# Vanilla OS Website - Edits by Gabs during High Seas

The changes made by me (Gabs), to Vanilla OS' website during High Seas.

## Changes by me

### Pay What You Want System

- **Pull Request**: [#281](https://github.com/Vanilla-OS/website/pull/281)

In the download page, it will ask you to make a donation, and the option do download the iso without any donation by writing “0” in the custom amount input. If you make a donation, then it will open a new tab with paypal, will create a 24 hour cookie locally noting that you have made a donation, refreshing the page, showing a special “Thank you” message, auto downloading the iso, and another button in case it doesn’t work.

### Directly Support Team Members

- **Pull Request**: [#277](https://github.com/Vanilla-OS/website/pull/277)

In the "Team" page, you can directly support a team member by clicking the "Support Me" button, which will either open a popup with the options to donate to the team member or a new tab to their only sponsors page. It's pretty smart, and it's a good way to support the team members directly.

### Snowflakes Decoration during Holidays

- **Pull Request**: [#268](https://github.com/Vanilla-OS/website/pull/268)

In the "Home" page, during the holidays (25th December to 1st January), snowflakes will fall from the top of the page. It's a nice touch to the website, and it's a good way to celebrate the holidays.

### Sort updates by date

- **Pull Request**: [#280](https://github.com/Vanilla-OS/website/pull/280)

In the "Updates" page, the updates are now sorted by date, so the latest updates will be shown first. It's a good way to keep the users updated with the latest news.

### Migrate the center tag to an class

- **Pull Request**: [#278](https://github.com/Vanilla-OS/website/pull/278)

Just a cleanup, the center tag is now a class, and it's a good way to keep the code clean, and using the center tag is not recommended.

---

<hr />
<p>This source code is distributed under the <a href="LICENSE">AGPL 3.0</a>
license, while Vanilla OS is a product of <a href="//fabricators.ltd" target="_blank">fabricators.ltd</a>.

Please note that all assets on this website are owned by fabricators.ltd and
the Vanilla OS Contributors Team.</p>

## Development

### CSS Convention

Our framework follows the [BEM (Block, Element, Modifier)](https://en.bem.info/methodology/quick-start/)
convention for CSS classes.

Colors are defined in the `assets/css/colors/default.css` and `assets/css/colors/dark.css`
files, they must be unique and not overlap with each other.

Each new component (block) must be defined in a separate file in the `assets/css/components`
directory and must follow the following structure:

```css
.block {
  /* Color Variables */
  --block-color: var(--color-primary);
  --block-element-color: var(--color-secondary);
}

.block {
  /* Block Styles */
  background-color: var(--block-color);
}

.block-element {
  /* Element Styles */
  background-color: var(--block-element-color);
  width: 100px;
  height: 100px;
}

.block--modifier {
  /* Modifier Styles */
  width: 200px;
  height: 200px;
}

/* Media Queries */
```

### Build and Run

To run the Vanilla OS website locally, you need to have [Vue.js](https://vuejs.org/) and
[Vite](https://vitejs.dev/) installed.

#### Build articles index

```bash
pnpm generate-articles
```

#### Run the website locally

This will also build the articles index.

```bash
pnpm dev
```

## Production Build

This will also build the articles index.

```bash
pnpm build
```
