## How to use static styles instead of dynamic ones

If you don't want styles to be editable from the admin area:

1. Replace the `settings_schema.json` with the one in the `src/config/static-styles` folder (after removing `_no_styles` from its filename).

2. Replace `@import './variables-dynamic';` with `@import './variables-static';` in the top of the `src/styles/variables.scss` file.

3. Delete the contents of the `src/snippets/css-variables.liquid`. Just its contents, not the file itself.

## How to add custom fonts.

1. Add your `@font-face` definitions in the `typography.scss` file.
2. Disable the setting "Theme Settings > Typography > Global > Use Shopify Fonts" in the Shopify Theme Editor.
3. Update the `font-` variables under the Typography section in either `variables-dynamic.scss` or `variables-static.scss`.

Just to make it clear: You CAN have dynamic styles without using Shopify's fonts.