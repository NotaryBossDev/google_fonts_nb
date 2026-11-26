# google_fonts_nb

An unmodified copy of [google_fonts](https://pub.dev/packages/google_fonts) **6.3.3** (BSD 3-Clause, see `LICENSE` and
`AUTHORS`) with one addition: `GoogleFonts.config.styleResolver`.

- `lib/src/google_fonts_all_parts.g.dart`: adds the nullable `styleResolver` field to `Config`.
- `lib/src/google_fonts_base.dart`: `googleFontsTextStyle` passes the created style to `styleResolver` (when set) and
  returns its result, or the original style when it returns null.

Nothing else differs from the published 6.3.3 package. With no resolver set, behaviour is identical to upstream.

Maintenance: when the consuming app moves to a newer google_fonts, re-apply the same two edits on top of that exact
upstream release, tag it, and pin consumers to the new commit.
