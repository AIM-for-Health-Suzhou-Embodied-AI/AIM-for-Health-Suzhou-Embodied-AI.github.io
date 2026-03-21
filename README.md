# AIM-for-Health-Suzhou-Embodied-AI.github.io

## Quick Start

```bash
bun install
bun run dev
```

## Project Structure

- `src/pages/index.astro`
  Homepage content, including:
  team members, lab intro, research directions, publications, and homepage images.
- `src/components/basic/Footer.astro`
  Footer content.
- `src/components/user/MemberCard.astro`
  Team member card rendering.
- `src/components/user/PublicationCard.astro`
  Publication card rendering.

## Pictures

Use `AIM_lab/public/images` for homepage and section images.

Recommended location:

- `public/images`
  Lab intro images, research direction images, publication preview images, footer collaborator logos.
- `public/avatar`
  Member headshots. This is the current location used by the homepage.

Examples already used on the homepage:

- `public/images/wormhole.png`
- `public/images/social-card.webp`
- `public/images/Digital Twins.png`

## Where To Change Image Paths

### 1. Lab intro image

The image in the `About The Lab` section is set directly in:

- `src/pages/index.astro`

Search for:

```astro
<img src='/images/wormhole.png' alt='Spatial Perception Research'
```

Replace `src` with your new path, for example:

```astro
src='/images/your-about-image.png'
```

### 2. Research direction images

Research direction card images are configured in:

- `src/pages/index.astro`

Search for:

```ts
const researchDirections = [
  {
    title: 'Multimodal World Model',
    image: '/images/wormhole.png'
  }
]
```

Each direction uses its own `image` field. Change that path to update the card image.

### 3. Publication preview images

Publication preview images are also configured in:

- `src/pages/index.astro`

Search for `previewImage`, for example:

```ts
previewImage: '/images/social-card.webp'
```

### 4. Member photos

Member photos are currently configured in:

- `src/pages/index.astro`

Search for:

```ts
const members = [
  {
    name: 'Zongyuan Ge',
    photo: '/avatar/zongyuan ge.png'
  }
]
```

If you want to move member photos into `public/images`, update `photo` accordingly, for example:

```ts
photo: '/images/zongyuan-ge.png'
```