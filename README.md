# Async Cookies API

This repository documents an API for accessing HTTP cookies asynchronously from
Document and Service Worker execution contexts.

* [The explainer](explainer.md) is a developer-oriented preview of the API.
* [The specification draft](https://wicg.github.io/cookie-store/) is aimed at
  browser developers.

The API has a test suite in the
[Web Platform Tests project](https://web-platform-tests.org/).

* Read the
  [test code](https://github.com/w3c/web-platform-tests/tree/master/cookie-store)
  for example usage.
* See the [test passing rates across browsers](https://wpt.fyi/cookie-store/).
* [Run the tests in your own browser](https://w3c-test.org/cookie-store/).


## Code

This API does not introduce new capabilities to the Web platform. In Document
contexts, it can be mostly polyfilled.

This repository includes a [proof-of-concept polyfill](cookies.js) with
[tests](https://wicg.github.io/cookie-store/cookies_test). The polyfill can be
used on insecure origins, but [some of the tests fail](http://wicg.github.io/cookie-store/cookies_test.html) due to their coverage of
`Secure` cookies.


## Resources

This API is inspired by and loosely based on the following discussions.

* https://github.com/slightlyoff/ServiceWorker/issues/707
* https://github.com/WICG/async-cookies-api/issues/14

The Async Cookies API has also been discussed in the following places.

* [WICG discourse thread](https://discourse.wicg.io/t/rfc-proposal-for-an-asynchronous-cookies-api/1652)
* [Blink intent-to-implement](https://groups.google.com/a/chromium.org/d/msg/blink-dev/gU-tSdjR4rA/hAYgmxiHCAAJ)

The best resource for understanding cookies is the latest draft of
[RFC 6265bis](https://tools.ietf.org/html/draft-ietf-httpbis-rfc6265bis-02).
