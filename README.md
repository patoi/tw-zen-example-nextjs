# Next.js + Tailwind CSS + TW Zen Example

This example shows how to use [Tailwind CSS](https://tailwindcss.com/) and [TW Zen](https://github.com/patoi/tw-zen) animation plugin with Next.js.

## Create animation

Add `plugin` and `safelist` in TailwindCSS configuration https://github.com/patoi/tw-zen-example-nextjs/blob/main/tailwind.config.js :

```text
  plugins: [require('tw-zen')],
  safelist: ['zen--suspend', 'zen--animate', 'zen--reduced']
```

Initialize TW Zen zero-dependency intersection handler with `useEffect` on the page, https://github.com/patoi/tw-zen-example-nextjs/blob/4ce6fd7709db3e190301dc9db54e60eeb27e490c/pages/index.tsx#L7-L11 :

```javascript
  useEffect(() => {
    import('tw-zen/init').then(twZenInit => {
      twZenInit.default()
    })
  }, [])
```

Add TW classes, for example: https://github.com/patoi/tw-zen-example-nextjs/blob/main/pages/index.tsx

```javascript
<h1 id="example-zen-fade" className="zen zen-fade ...">

<div id="example-zen-spin-forever" className="zen zen-spin-forever ...">🌟</div>

<a id="example-zen-pop-up-always" className="zen zen-pop-up ...">

<a id="example-zen-pop-up-only-once" className="zen zen-once zen-pop-up ...">

<a id="example-zen-from-left" className="zen zen-from-left...">

<a id="example-zen-from-left" className="zen zen-from-right...">

<Image id="example-zen-spin-with-pause" className="zen zen-pause zen-spin-forever" ...>
```


