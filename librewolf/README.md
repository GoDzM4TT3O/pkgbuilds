## librewolf

This LibreWolf version was modified in order to allow Google Meet (and similar websites) to work.
NOTE: if you don't have to use it, please disable the appropriate lines in the `PKGBUILD`! (See lines below)

+ Patch features:
	- Enable CTRL+C & CTRL+V detection (Disable if not used!!)
	- Enable HTTP(S) pipelining (faster speeds)
	- Enable `dom.webaudio.enabled` and `media.peerconnection.enabled`, to fix Google Meet (Disable if not used!!)
	- Enable devtools dark theme
	- Enable webcam (Disable if not used!!)
	- Fixed `LDFLAGS`
	- Only send "scheme+host+port" in the referer, nothing more, nothing less
	- Remove unnecessary search engines: DuckDuckGo Lite, Startpage, Jive Search, Qwant, MetaGer; The only 2 search engines left are DDG and Searx
