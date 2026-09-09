# Strata issue #699: Qt Save As filename

Before/after screenshots for https://github.com/lgse/strata/issues/699.

Both images use the same generic `SaveFile` request: `current_file` names a new
`packing-list-格式.xls` inside an accessible Downloads folder; `current_folder`
is Downloads; `current_name` is absent. No file is created by the demonstration.

- **Before:** official Strata 0.14.0-rc.1 release binary. Home is shown and Name is blank.
- **After:** a local build from source commit 916095a (0.13.0) with the compatibility fix. Downloads is
  shown and Name contains the suggested filename, including Unicode and extension.

These are direct captures of the real GTK chooser on isolated Xvfb and private
D-Bus sessions, using disposable folders and preferences. No personal files are
shown. The PR ports the same resolver change to current main, where the original
resolver behavior is unchanged.

The before binary was verified byte-for-byte against the official 0.14.0-rc.1
release archive (SHA-256 of the executable:
`06fb00060fdc668eb4ad0eb26e7fadf1acfbefd87e9f12aba5d00e569d64badb`).
The two builds differ in unrelated UI details; the identical request demonstrates
the filename and initial-folder behavior addressed by this PR.
