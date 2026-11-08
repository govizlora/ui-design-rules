# UI Design Rules

Simple UI design rules that almost always apply, unless you’re building [art](https://en.wikipedia.org/wiki/Casa_Mil%C3%A0).

## Element should have spacing from its container

![Leave space between an element and container edges unless their contours match](assets/space-from-container.svg)

Spacing is not required for sections that extend to the container edges and follow its contour:

![Edge-to-edge sections are acceptable when they follow the rounded or square container contour](assets/contour-match.svg)

## Element should have equal x and y spacing from its container edges

![A corner element should have equal horizontal and vertical insets, not unequal insets](assets/equal-spacing-regular.svg)

This applies regardless of element or container shape:
![A circular element also needs equal horizontal and vertical insets from its container edges](assets/equal-spacing-circle.svg)

The same principle applies when an element is inset from multiple edges:
![A nested panel should have equal left, right, and bottom insets, not narrower side insets](assets/equal-spacing-surface.svg)

## Spacing between items should match their spacing from the container

By default, items in a group should have the same spacing between each other as they have from the container edges.

Smaller gaps are acceptable when items are functionally related or need to read as a distinct group. This follows the proximity principle in [Gestalt psychology](https://en.wikipedia.org/wiki/Gestalt_psychology): items placed closer together are perceived as belonging together. Otherwise, keep the gaps equal to the container padding.

Gaps within the same group should never be larger than the spacing from the container edges.

![With 16px container padding, a 16px item gap is recommended, 8px is acceptable for functional grouping, and 32px is not](assets/item-gap-and-padding.svg)

## Element should be concentric to its container

The ideal element radius can be calculated as `elementRadius = containerRadius - inset`. For example, if `containerRadius = 32px` and `inset = 16px`, the ideal `elementRadius` is `16px`.

![With a 32px outer radius and 16px inset, a 16px inner radius is ideal, 24px is acceptable, and 8px is not](assets/concentric.svg)

When choices are limited, an `elementRadius` that is slightly larger than the ideal radius is acceptable. Never use a radius smaller than the ideal value.
