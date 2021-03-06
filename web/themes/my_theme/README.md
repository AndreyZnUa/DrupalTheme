<!-- @file Instructions for subtheming using the Sass Starterkit. -->
<!-- @defgroup sub_theming_sass -->
<!-- @ingroup sub_theming -->
# Sass Starterkit

Below are instructions on how to create a Bootstrap sub-theme using a Sass
preprocessor.

- [Prerequisites](#prerequisites)
- [Additional Setup](#setup)
- [Overrides](#overrides)

## Prerequisites
- Read the @link getting_started Getting Started @endlink and
  @link sub_theming Sub-theming @endlink documentation topics.
- You must understand the basic concept of using the [Sass] CSS pre-processor.
- You must use a **[local Sass compiler](https://www.google.com/search?q=sass+compiler)**.
- You must use the [Bootstrap Framework Source Files] ending in the `.scss`
  extension, not files ending in `.css`.

## Additional Setup {#setup}
Download and extract the **latest** 3.x.x version of
[Bootstrap Framework Source Files] into the root of your new sub-theme. After
it has been extracted, the directory should be renamed (if needed) so it reads
`./my_theme/bootstrap`.

If for whatever reason you have an additional `bootstrap` directory wrapping the
first `bootstrap` directory (e.g. `./my_theme/bootstrap/bootstrap`), remove the
wrapping `bootstrap` directory. You will only ever need to touch these files if
or when you upgrade your version of the [Bootstrap Framework].

{.alert.alert-warning} **WARNING:** Do not modify the files inside of
`./my_theme/bootstrap` directly. Doing so may cause issues when upgrading the
[Bootstrap Framework] in the future.

## Overrides {#overrides}
The `./my_theme/scss/_default-variables.scss` file is generally where you will
spend the majority of your time providing any default variables that should be
used by the [Bootstrap Framework] instead of its own.

The `./my_theme/scss/overrides.scss` file contains various Drupal overrides to
properly integrate with the [Bootstrap Framework]. It may contain a few
enhancements, feel free to edit this file as you see fit.

The `./my_theme/scss/style.scss` file is the glue that combines:
`_default-variables.scss`, [Bootstrap Framework Source Files] and the 
`overrides.scss` file together. Generally, you will not need to modify this
file unless you need to add or remove files to be imported. This is the file
that you should compile to `./my_theme/css/style.css` (note the same file
name, using a different extension of course).

#### See also:
- @link theme_settings Theme Settings @endlink
- @link templates Templates @endlink
- @link plugins Plugin System @endlink

[Bootstrap Framework]: https://getbootstrap.com/docs/3.3/
[Bootstrap Framework Source Files]: https://github.com/twbs/bootstrap-sass
[Sass]: http://sass-lang.com
