# Position `absolute`

* An element with `position: absolute`; is positioned `relative` to the nearest positioned ancestor (instead of positioned `relative` to the viewport, like fixed).
* However; if an `absolute` positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.
* __Note__: `absolute` positioned elements are removed from the normal flow, and can overlap elements.