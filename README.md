# Spoon Builder

This script copies files to the RailsBridge Boston USB drives. If you're
on a Mac, run:

    ./build-spoons

On Linux, pass the path to where your USB drives are mounted:

    ./build-spoons /media/usb0 /media/usb1 # etc...

# Getting started

If you have an old USB drive, copy all the files on it (from all
directories) to the `cache` directory. This will speed up the process so
that you don't need to re-download any that haven't changed.

# Troubleshooting

If you get the error:

    certificate verify failed (OpenSSL::SSL::SSLError)

trying to download a file, your version of Ruby may have an out-of-date
CA certificate bundle. Try updating Ruby to at least 2.3.0.

# Adding new USB drives to the collection

New drives should be formated with a name starting with `RBB` and then a
number.

# Updating files for the next workshop

TODO: write this section.
