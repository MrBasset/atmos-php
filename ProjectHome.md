PHP wrapper for connecting to EMC Atmos Cloud Storage

## New Version: 2.1.1 ##
  * Added missing file AccessTokens.php

## Previous Version: 2.1.0 ##
  * Added support for Atmos 2.1.0 features
    * Keypools
    * Shareable URLs with Content-Disposition
    * New hashing algorithms: SHA1, MD5 (requires PHP 5.1.2+)
    * Anonymous access tokens
  * Added support for UTF-8 encoded headers (Atmos 2.0.1+)
  * Fixed a couple failing unit tests

## Previous Version: 1.4.1.21 ##
  * Added support for PHP 5.1.6 and higher.
  * Added support for tokens and limits when listing / reading from objects.
  * Added support for fetching metadata when listing / reading from objects.
  * Improved error handling.
  * Added support for operations on the root directory.
  * Improved support for listing object versions.
  * Cleanup after failed zero-byte downloads.
  * Progress Listener improvements.

## Older Version: 1.4.1.20 ##
  * Added support for retrieving ContentType and Object Checksum values
  * Improved ProgressListener class functionality
  * Unicode filenames are no longer rejected
  * Eliminated use of deprecated functions split() and ereg(), and cleaned up other deprecated warnings.
  * Unix download packages are now available
  * Bug fixing in SHA0.php for 32-bit platform support.
  * Fixed bug in SHA0.PHP line 283 -- improper parameters passed to str\_pad()
  * Various other bug fixes

## Older Version: 1.4.0.16 ##
  * Added support for monitoring the underlying HTTP protocol request/response messages.
  * Added support for setting the user agent.

## Older Version: 1.4.0.15 ##
  * Added support for metadata with multiple values
  * Fixed undefined index errors in EsuObjects.php
  * Silenced error reporting for calls to fopen()

## Older Version: 1.4.0.12 ##
  * Fixed a URL encoding issue with parenthesis

## Older Version: 1.4.0.10 ##
  * Fixed SSL connection failure on some Linux hosts
  * Fixed HTTP redirection handling
  * Fixed callbacks on helpers to properly report progress

### Older Version: 1.4.0.7 ###
  * New release to support Atmos 1.4 Features
    * Checksum support on upload and download for erasure coded replicas
    * Support for Versioning
    * Rename object in namespace
    * Get service information (Atmos version)
    * Get Object Info (replicas, retention, and deletion info)
  * Bugfixes
    * Better support for reading and writing most Unicode characters in metadata
    * Fixed whitespace normalization when computing signatures (metadata with multiple consecutive spaces would fail)
    * UploadHelper can set the object MIME type.
  * Upgraded: the PHP wrapper now uses HTTP\_Request2 instead of the deprecated HTTP\_Request package.  This should allow for better performance with alternate back ends (e.g. libcurl)


Older Release: 1.2.5.3
  * Fixed getShareableUrl()