[**API**](../../API.md)

***

# Interface: WindowVirtualizerProps

Props of [WindowVirtualizer](../functions/WindowVirtualizer.md).

## Properties

### children

> **children**: `ReactNode` \| (`index`) => `ReactElement`\<`any`, string \| JSXElementConstructor\<any\>\>

Elements rendered by this component.

You can also pass a function and set [WindowVirtualizerProps.count](WindowVirtualizerProps.md#count) to create elements lazily.

#### Defined in

[src/react/WindowVirtualizer.tsx:63](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L63)

***

### count?

> `optional` **count**: `number`

If you set a function to [WindowVirtualizerProps.children](WindowVirtualizerProps.md#children), you have to set total number of items to this prop.

#### Defined in

[src/react/WindowVirtualizer.tsx:67](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L67)

***

### overscan?

> `optional` **overscan**: `number`

Number of items to render above/below the visible bounds of the list. Lower value will give better performance but you can increase to avoid showing blank items in fast scrolling.

#### Default Value

```ts
4
```

#### Defined in

[src/react/WindowVirtualizer.tsx:72](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L72)

***

### itemSize?

> `optional` **itemSize**: `number`

Item size hint for unmeasured items. It will help to reduce scroll jump when items are measured if used properly.

- If not set, initial item sizes will be automatically estimated from measured sizes. This is recommended for most cases.
- If set, you can opt out estimation and use the value as initial item size.

#### Defined in

[src/react/WindowVirtualizer.tsx:79](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L79)

***

### shift?

> `optional` **shift**: `boolean`

While true is set, scroll position will be maintained from the end not usual start when items are added to/removed from start. It's recommended to set false if you add to/remove from mid/end of the list because it can cause unexpected behavior. This prop is useful for reverse infinite scrolling.

#### Defined in

[src/react/WindowVirtualizer.tsx:83](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L83)

***

### horizontal?

> `optional` **horizontal**: `boolean`

If true, rendered as a horizontally scrollable list. Otherwise rendered as a vertically scrollable list.

#### Defined in

[src/react/WindowVirtualizer.tsx:87](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L87)

***

### cache?

> `optional` **cache**: [`CacheSnapshot`](CacheSnapshot.md)

You can restore cache by passing a [CacheSnapshot](CacheSnapshot.md) on mount. This is useful when you want to restore scroll position after navigation. The snapshot can be obtained from [WindowVirtualizerHandle.cache](WindowVirtualizerHandle.md#cache).

**The length of items should be the same as when you take the snapshot, otherwise restoration may not work as expected.**

#### Defined in

[src/react/WindowVirtualizer.tsx:93](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L93)

***

### ssrCount?

> `optional` **ssrCount**: `number`

A prop for SSR. If set, the specified amount of items will be mounted in the initial rendering regardless of the container size until hydrated.

#### Defined in

[src/react/WindowVirtualizer.tsx:97](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L97)

***

### as?

> `optional` **as**: [`CustomContainerComponent`](../type-aliases/CustomContainerComponent.md) \| keyof IntrinsicElements

Component or element type for container element.

#### Default Value

```ts
"div"
```

#### Defined in

[src/react/WindowVirtualizer.tsx:102](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L102)

***

### item?

> `optional` **item**: [`CustomItemComponent`](../type-aliases/CustomItemComponent.md) \| keyof IntrinsicElements

Component or element type for item element. This component will get [CustomItemComponentProps](CustomItemComponentProps.md) as props.

#### Default Value

```ts
"div"
```

#### Defined in

[src/react/WindowVirtualizer.tsx:107](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L107)

***

### onScroll()?

> `optional` **onScroll**: () => `void`

Callback invoked whenever scroll offset changes.

#### Returns

`void`

#### Defined in

[src/react/WindowVirtualizer.tsx:111](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L111)

***

### onScrollEnd()?

> `optional` **onScrollEnd**: () => `void`

Callback invoked when scrolling stops.

#### Returns

`void`

#### Defined in

[src/react/WindowVirtualizer.tsx:115](https://github.com/inokawa/virtua/blob/d2c1d3653c8c81252d5e36872bda7c628b56b149/src/react/WindowVirtualizer.tsx#L115)
