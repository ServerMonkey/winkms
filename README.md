winkms(1) -- Windows KMS key finder
=============================================

## SYNOPSIS

`winkms <ACTION> <PARAMETER> [<URL>]`

## DESCRIPTION

Find Windows KMS activation keys.

## OPTIONS

* `-h`, `--help` :
  Displays the help screen.
* `find <SEARCH_STRING>` : Search for a specific key. If there is no database
  file, winkms will autoupdate first.
* `update [URL]` : Update the database file from an optional URL. Files will be
  saved to '~/.winkms/'. When updating without a URL argument, archive.org will
  be used instead of microsoft.com or windowsafg.com. This is more reliable
  than the original URL. The original URLs are
  https://docs.microsoft.com/en-us/windows-server/get-started/kms-client-activation-keys
  and https://www.windowsafg.com/keys.html . If you use a URL das does not
  contain the string 'microsoft' or 'windowsafg', the file will be downloaded
  to misc.txt. Use this to add your own keys. First line is the OS name and the
  second line the key.
* `browse` : Look at all the keys by opening all database files in the default
  browser.

The database is made of three files:

- default.htm - Default Generic keys from windowsafg.com
- kms.htm - Official GVLK and KMS keys from microsoft.com
- misc.txt - Custom user keys

## EXAMPLES

Search for Windows 7 Pro

    $ winkms find '7 Pro'

Search for Windows 10 Pro

	$ winkms find '10/11 Pro'

First update the database via archive.org,  
then update the KMS keys database via microsoft.com

    $ winkms update
    $ winkms update https://learn.microsoft.com/en-us/windows-server/get-started/kms-client-activation-keys

## COPYRIGHT

See license file

## SEE ALSO

curl(1)
