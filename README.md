# useSortable options type error

This repo demonstrates a TypeScript type error when using `useSortable` from `@vueuse/integrations/useSortable`.

[![status][workflow-img]][workflow-url]

## Steps

```sh
pnpm install
pnpm run lint:ts
```

```sh
src/App.vue:15:1 - error TS2769: No overload matches this call.
  Overload 1 of 2, '(selector: string, list: MaybeRef<{ id: number; name: string; }[]>, options?:
    Argument of type 'Readonly<ShallowRef<HTMLDivElement | null, HTMLDivElement | null>>' is not assignable to parameter of type 'string'.
  Overload 2 of 2, '(el: MaybeRefOrGetter<MaybeElement>, list: MaybeRef<{ id: number; name: string; }[]>, options?: UseSortableOptions | undefined): UseSortableReturn', gave the following error.
    Object literal may only specify known properties, and 'animation' does not exist in type 'UseSortableOptions'.
```

## Versions

```md
node: v24.13.0

vue: 3.5.32
@vueuse/core & @vueuse/integrations: 14.2.1
sortablejs: 1.15.7
typescript: 6.0.2
```

[workflow-img]: https://img.shields.io/github/actions/workflow/status/VChet/vueuse-usesortable-repro/.github/workflows/lint.yaml
[workflow-url]: https://github.com/VChet/vueuse-usesortable-repro/actions/workflows/lint.yaml
