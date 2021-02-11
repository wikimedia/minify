# Changelog

## 2.0.0 (2021-02-08)

This release requires PHP 7.2+, and drops support for Internet Explorer 6-10.

Added:

* CSSMin: Support multiple `url()` values in one rule. (Bartosz Dziewoński)
* CSSMin: Support embedding of SVG files. (m4tx)

Removed:

* JavaScriptMinifier: Remove support for the `$statementsOnOwnLine` option.
* JavaScriptMinifier: Remove support for the `$maxLineLength` option.
* CSSMin: Remove data URI fallback, previously for IE 6 and IE 7 support.

Changed:

* CSSMin: Reduce SVG embed size by using URL-encoding instead of base64-encoding. (Bartosz Dziewoński)
* CSSMin: Improve SVG compression by preserving safe literals. (Roan Kattouw, Volker E, Fomafix)

Fixed:

* CSSMin: Fix non-embedded URLs that are proto-relative or have query part. (Bartosz Dziewoński) [T60338](https://phabricator.wikimedia.org/T60338)
* CSSMin: Avoid corruption when CSS comments contain curly braces. (Stephan Gambke) [T62077](https://phabricator.wikimedia.org/T62077)
* CSSMin: Avoid corrupting parenthesis and quotes in URLs. (Timo Tijhof) [T60473](https://phabricator.wikimedia.org/T60473)
* CSSMin: Skip remapping for special `url(#default#behaviorName)` values. (Julien Girault)
* JavaScriptMinifier: Fix "Uninitialized offset" in string and regexp parsing. (Timo Tijhof) [T75556](https://phabricator.wikimedia.org/T75556)
* JavaScriptMinifier: Fix "Uninitialized offset" in regexp char class parsing. (Timo Tijhof) [T75556](https://phabricator.wikimedia.org/T75556)
* JavaScriptMinifier: Fix possible broken `return` statement after a ternary in a property value. (Timo Tijhof) [T201606](https://phabricator.wikimedia.org/T201606)

## 1.0.0 (2011-11-23)

Initial release, originally bundled with MediaWiki 1.19.
