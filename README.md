winkms(1) -- Windows KMS key finder
=============================================

## SYNOPSIS

`winkms <ACTION> <PARAMETER>`

## DESCRIPTION

Find Windows KMS activation keys.

## OPTIONS

* `-h`, `--help` :
  Displays the help screen.
* `find <SEARCH_STRING>` : Search for a specific key. If there is no database
  file, winkms will autoupdate first.
* `update [URL]` : Update the database file from a URL. File will be saved
  to '~/.winkms/keys.html'. The original URL
  is https://docs.microsoft.com/en-us/windows-server/get-started/kms-client-activation-keys
  But due to Microsoft changing the URL now and then, the archive.org cache
  will be used. Which is more reliable. Optional: Any URL can be specified. For
  example or an older version from archive.org
* `browse` : Look at all the keys. Opens the database (HTML file) with the
  default desktop application.

## EXAMPLES

Search for Windows 7 Pro

    $ winkms find '7 Pro'

Update the database via microsoft.com

    $ winkms update https://learn.microsoft.com/en-us/windows-server/get-started/kms-client-activation-keys

## COPYRIGHT

See license file

## SEE ALSO

curl(1)
