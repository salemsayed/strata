# Strata issue #699: Qt Save As filename

Before/after screenshots for https://github.com/lgse/strata/issues/699.

Both images use the same generic `SaveFile` request: `current_file` names a new
`packing-list-格式.xls` inside an accessible Downloads folder; `current_folder`
is Downloads; `current_name` is absent. No file is created by the demonstration.

- **Before:** Strata 0.13.0 release binary. Home is shown and Name is blank.
- **After:** the same version with the local compatibility fix. Downloads is
  shown and Name contains the suggested filename, including Unicode and extension.

These are direct captures of the real GTK chooser on isolated Xvfb and private
D-Bus sessions, using disposable folders and preferences. No personal files are
shown. The PR ports the same resolver change to current main, where the original
resolver behavior is unchanged.
