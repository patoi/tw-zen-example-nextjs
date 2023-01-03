# Next.js + Tailwind CSS + TW Zen Example

This example shows how to use [Tailwind CSS](https://tailwindcss.com/) and [TW Zen](https://github.com/patoi/tw-zen) animation plugin with Next.js.

## Create animation

1. Add `plugin` and `safelist` in TailwindCSS configuration https://github.com/patoi/tw-zen-example-nextjs/blob/main/tailwind.config.js :

```text
  plugins: [require('tw-zen')],
  safelist: ['zen--suspend', 'zen--animate', 'zen--reduced']
```

2. Initialize TW Zen zero-dependency intersection handler with `useEffect` on the page:

```javascript
  useEffect(() => {
    import('tw-zen/init').then(twZenInit => {
      twZenInit.default()
    })
  }, [])
```

3. Add TW classes, for example: https://github.com/patoi/tw-zen-example-nextjs/blob/main/pages/index.tsx

```javascript
<h1 id="example-zen-fade" className="zen zen-fade ...">

<div id="example-zen-spin-forever" className="zen zen-spin-forever ...">🌟</div>

<a id="example-zen-pop-up-always" className="zen zen-pop-up ...">

<a id="example-zen-pop-up-only-once" className="zen zen-once zen-pop-up ...">

<a id="example-zen-from-left" className="zen zen-from-left...">

<a id="example-zen-from-left" className="zen zen-from-right...">

<Image id="example-zen-spin-with-pause" className="zen zen-pause zen-spin-forever" ...>
```

Read more about classes: https://github.com/patoi/tw-zen/blob/master/README.md
