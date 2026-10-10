---
name: nika-business
description: Use when working for one of the user's businesses in Nika — anything visual or customer-facing (sites, pages, components, emails, posts, decks, ads, docs), naming, copy, or choices that depend on the business. Loads the business's profile and brand kit from Nika so you use its real logo, tagline, colors and fonts.
---

# Working for a Nika business

1. If you don't know which business, call `list_businesses` (Nika tools). Ask the user only when it's ambiguous and it matters.
2. Call `get_business` with that business's id (`"personal"` is the user's own business).
3. Use the business's own brand in everything you make for it:
   - `name`, `tagline`, `logo_url` and `website` exactly as given.
   - `brand_kit` colors: `primary`, `secondary`, `accent`. Fonts: `font_display` for headings, `font_body` for body text.
   - Never invent a different palette, font, logo or tagline. If the brand kit is empty, say so and keep the styling neutral. Don't make one up.
4. Write for the business's `target_customer`, in a voice that fits `what_it_does`.
5. When the work is a deliverable the user should keep, save it with `save_to_library` (see the nika-library skill).
