# UI Design Rules

## Element should have equal x and y spacing from its container edges

![Equal corner spacing regular case](assets/equal-spacing-regular.svg)

This applies regardless of element or container shape:
![Equal corner spacing circle case](assets/equal-spacing-circle.svg)

The same principle applies when an element is inset from multiple edges:
![Equal corner spacing surface case](assets/equal-spacing-surface.svg)

## Element should be concentric to its container

The ideal element radius can be calculated as `elementRadius = containerRadius - inset`. For example, if `containerRadius = 32px` and `inset = 16px`, the ideal `elementRadius` is `16px`.

![Concentric case](assets/concentric.svg)

When choices are limited, an `elementRadius` that is slightly larger than the ideal radius is acceptable. Never use a radius smaller than the ideal value.
