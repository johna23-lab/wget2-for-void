Wget2 is the successor of GNU Wget, a file and recursive website downloader.

Designed and written from scratch it wraps around libwget, that provides the basic functions needed by a web client.

Wget2 works multi-threaded and uses many features to allow fast operation.

In many cases Wget2 downloads much faster than Wget due to HTTP2, HTTP compression, parallel connections, use of If-Modified-Since HTTP header and more.

Wget2 has several new command-line options, see the wiki page for a list and comparison with Wget.

Wget will be maintained further. The idea is that breaking changes and new functionalities go into Wget2 / libwget.

Except for WARC and FTP, Wget2 is a drop-in replacement for Wget in most cases.
Of course there may be subtle differences, so make sure to test well before replacing Wget by Wget2.

GNU Wget2 is licensed under GPLv3+. Libwget is licensed under LGPLv3+.

**Noteworthy changes since the last release (see also the NEWS file):**

  * New option --follow-sitemaps
  * New option --dane (cert validation via DNS)
  * Implement --check-certificate=quiet
  * Support proxies on non-default ports
  * Added CIDR support for no_proxy (IPv4 and IPv6)
  * Improve recursive RSS/Atom processing
  * Improve default cert/bundle paths for Windows
  * Improve Windows and MSVC compatibility
  * Use CONNECT for https_proxy
  * Add decoding numeric XML entities
  * Improve OpenSSL code
  * Improve WolfSSL code
  * Improve the progress bar
  * New function wget_xml_decode_entities_inline()
  * Support compilation of wget.h from C++
  * Handle comments in robots.txt correctly
  * Fix parsing HTMP/XML entities in URLs from HTML/XML
  * Fix use-after-free when updating blacklist entries
  * Don't try setting file timestamps on ttys
  * Fix arguments parsing for --filter-urls
  * Fix removing fragments when converting links
  * Fix duplicate downloads for Link headers with rel=duplicate
* Fix segmentation fault (NULL dereference when no HTTP header has been received)
  * Change arguments of wget_iri_compare to const
  * Fix memory leak in wget_hashmap_clear()
  * Extend network error messages with hostname and IP address
  * Fix status code for 5xx errors
  * Fix issue in wget_buffer_trim()
  * Improve tests, documentation, building
