# Spoon Builder

This script copies files to the RailsBridge Boston USB drives. If you're
on a Mac, run:

    ./build-spoons

On Linux, pass the path to where your USB drives are mounted:

    ./build-spoons /media/usb0 /media/usb1 # etc...

# Getting started

If you have an old USB drive, copy all the files on it to the `cache`
directory (don't copy folders containing the files, but copy the individual
files into `cache`) . This will speed up the process by preventing you from
having to re-download any files that haven't changed.

If you have an updated USB handy, this can be accomplished with (assuming it's
labeled `RBB01`):

    find /Volumes/RBB01/* -type f -exec rsync '{}' cache ';'

# Updating files for the next workshop

1. Open up `files.yml`.
1. Change the `railsbridgebm-YYYY-MM.box` key to the new box name.
1. Change the download URL for that box.
1. Save and run `./build-spoons`.

Make sure you make a new commit for these updates! (We should probably make this
more dynamic so that we don't have to change th code every time...)

# Troubleshooting

If you get the error:

    certificate verify failed (OpenSSL::SSL::SSLError)

trying to download a file, your version of Ruby may have an out-of-date
CA certificate bundle. Try updating Ruby to at least 2.3.0.

# Adding new USB drives to the collection

New drives should be formated with a name starting with `RBB` and then a
number.
