# Digital implementation

Read this reference for websites, apps, admin tools, and coded prototypes.

## Preserve the product first

Before restyling, map the target's required navigation, search, filters, forms, tables, editing, saving, upload, pagination, permissions, and responsive behavior. Preserve those capabilities and their information hierarchy unless the brief explicitly changes them. Adapt to the existing framework and component conventions instead of replacing the stack for visual reasons.

## Reuse the supplied assets

The reusable CSS entrypoint is `assets/css/styles.css`. It imports the files under `assets/css/tokens/` and provides `yed-` utility and component classes. The CSS loads Noto Serif SC, Cormorant Garamond, and Parisienne from Google Fonts with system fallbacks.

When integrating into another repository:

1. Copy the required `assets/css/` and `assets/brand/` files into a stable project-owned location.
2. Update relative image URLs if the destination layout differs.
3. Import the copied `styles.css` from the target's normal style entrypoint.
4. Map existing design tokens to the Yan Er Ding variables where possible. Do not duplicate an entire styling system when a small theme layer is sufficient.
5. Use target-native components and semantics; the supplied classes are a visual reference, not a framework requirement.

Do not reference files from a user's home directory or from the installed skill at runtime. If remote fonts are unavailable, retain the documented serif fallbacks rather than substituting a generic sans-serif brand face.

When the user asks for a `standalone HTML` without further constraints, default to one `.html` file with its necessary CSS, JavaScript, and packaged logo embedded. Remote Google Fonts may remain optional with documented serif fallbacks. If the user says offline or self-contained, remove all network dependencies as well.

For a greenfield brief that omits routes or catalog structure, use the smallest useful navigation and local or inert targets marked as provisional. Never invent production URLs or imply that a placeholder CTA is connected to a live catalog.

## Surface guidance

### Customer-facing

- Treat the page like a lookbook or boutique window: strong product imagery, composed groups, restrained copy, and a clear primary action.
- A useful hero pairs a concise text block with one focal product or uses one strong photograph with a legible action. Do not waste the first viewport on empty atmosphere.
- Product grids default to two columns on mobile when labels remain readable. Keep product images at `3:4` and protect the shoe silhouette.
- When many categories exist, prefer horizontally scrollable chips or a compact secondary filter over an overflowing tab row.

### Staff and admin

- Increase information density while retaining burgundy surfaces, gold rules, and serif typography. Do not turn the tool into a gray-white generic dashboard.
- Tables, forms, empty states, errors, loading, pagination, and permissions remain first-class. Brand styling must not reduce scan speed or conceal status.
- Use semantic status colors only where the state meaning needs them; keep decorative surfaces inside the burgundy/gold system.
- Buttons follow a clear hierarchy: gold-fill primary, transparent gold-border secondary, low-weight text action.

## Interaction and accessibility

- Keep semantic HTML, accessible names, visible keyboard focus, disabled states, and sufficient hit areas.
- Do not rely on color alone for status. Pair color with text or a meaningful icon.
- Check contrast in the real render. The palette tokens are a starting point, not proof that every opacity combination is legible.
- Avoid animations of layout properties. Use restrained opacity, transform, or clip effects and provide `prefers-reduced-motion` behavior.
- Ensure menus, dialogs, and popovers are not clipped by an ancestor with `overflow: hidden`.
- Use balanced wrapping for display headings and test actual Chinese copy at every breakpoint.

## Visual acceptance checklist

- Required workflows still complete successfully.
- The page uses burgundy as its field and gold as structure or emphasis, without decorative extra hues.
- Real logo artwork is clear, undistorted, and surrounded by safe space.
- Chinese headings and body copy retain a serif character; prices and short English display text use the designated display face.
- Images are not stretched, important shoe shapes are not cropped away, and lazy loading does not cause broken layout.
- Desktop and mobile have no overlap, clipping, overflow, inaccessible controls, or illegible text.
- Hover, focus, active, disabled, loading, empty, success, and error states are coherent where applicable.
- Reduced-motion mode remains usable and content is visible without animation.
