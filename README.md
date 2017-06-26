
# Writing

## Preparation
  * Make sure you can explain what is wrong or why a new entry is needed.
  * Before proposing a release notes entry about a concerns a software bug,
    make sure that the software bug itself is reported on Bugzilla.

## Getting the Change In
If you see an issue or want to add an entry, you can contribute in two ways:

* Create a [bug report](https://bugzilla.opensuse.org/enter_bug.cgi?&product=openSUSE%20Distribution&component=Release%20Notes&short_desc=[rn]+&assigned_to=sknorr%40suse.com).
  You will need an openSUSE account to do so.
  * Make sure to mention the affected openSUSE version.
  * If you are proposing a new entry, create a draft entry.

* Create a pull request on GitHub. You will need a GitHub account to do so.
  * Edit the file `xml/release-notes.xml` only. Language (PO) files will be
    created using [Weblate](https://l10n.opensuse.org/projects/release-notes-opensuse/)
    and `NEWS` is updated only directly before packaging.
  * Make sure to pick the right branch to base your contribution on. `master` is
    used for openSUSE Tumbleweed release notes, `Leap_*` branches are used for
    openSUSE Leap versions. Usually, the default branch will be the current
    development version of openSUSE Leap.

# Translating

To translate openSUSE release notes, use [Weblate](https://l10n.opensuse.org/projects/release-notes-opensuse/).

# Building

## Build Requirements

- `make`
- `daps` & `suse-xsl-stylesheets`
- `xsltproc`
- `w3m`
- `dejavu-fonts` & `google-opensans-fonts`
- `gettext-tools`
- `xml2po`
- `xmlcharent`

## Manual Build
* To produce the output formats, we use DAPS (package `daps`) and the SUSE
  DocBook stylesheets (package `suse-xsl-stylesheets`).
* When the above dependencies are satisfied, you can create output using:

  ```
  make linguas
  make all
  ```

## Build Service Build
* On the [build service](https://build.opensuse.org), search for the package
  `release-notes-openSUSE`.


# Publishing

* The release notes are available packaged within the distribution and on the
  Web.

* Package:
  * The name of package is `release-notes-openSUSE`.
  * The package is throughout the maintenance period of the distribution
    whenever need arises.

* Web Version:
  * The web version is built in the [OBS Project Documentation:Auto](https://build.opensuse.org/project/show/Documentation:Auto).
  * It is synced to the [documentation server](https://doc.opensuse.org/release-notes)
    using the scripts contained in the directory `tools` in this repository's
    `master` branch.

# More Information

Find general information about the release notes at
[https://en.opensuse.org/openSUSE:Release_Notes](https://en.opensuse.org/openSUSE:Release_Notes).
