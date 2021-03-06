Node-bell Changelog
===================

v0.6.0
------

- Upgrade node-ssdb to v0.1.6 (with spp_node, super fast now)

v0.5.9
------

- Upgrade tj/co to v4.1.0 (memory leaks fixed) (issue#70)

v0.5.8
------

- Bind unfinished data to connection object (#74)

v0.5.7
------

- Add cache for listener#match

v0.5.5 (v0.5.6)
---------------

- Rewrite hipchat alerter (alert by patterns)
- User strftime as log datetime

v0.5.4
-------

- Fix analyzers memory leaks.

v0.5.3 (v0.5.1 v0.5.2)
-----------------------

- Upgrade node-ssdb to v0.1.5
- Add ssdb connection pool support
- Fix alerter hipchat

v0.5.0
------

- Reback to `upper_90` from `mean_90` as default timer field in statsd client

v0.4.9 (Fix 0.4.8)
------------------

- Rebuild a simple hipchat alerter

v0.4.7
------

- Fix typo `log.name` in bell.js
- Add how to run analyzers on more than 1 machine

v0.4.6
------

- Upgrade co to v4
- Upgrade node-ssdb to v0.1.4
- Remove bunyan logger, use our own simple logger
- Lots of dependencies version fixes.
- Command line usage changes: 1~5 for debug ~ fatal

v0.4.5
------

- Remove docs/conf.md
- Add comment documentation in config/configs.toml
- Add configuration `listener.blacklist`

v0.4.4
------

- Use nunjucks instead of swig as template engine.
- Lots of views and static/css style & typos fixes

v0.4.3
------

- Built in cluster support for webapp & analyzer #57

v0.4.1
------

- Merge all patterns to one place `patterns.js`
- add trend to enters

v0.4.0
------

- Revert to old `pattern` way instead of `prefix` way

v0.3.9
------

- Use `prefix` to filter & query metrics, instead of `pattern`. issue#51

v0.3.8
------

- Add clients for py, rb, path change: 'upstream' => 'clients'
- Add `cache` for webapp, issue#41, commit#3e1d7272cb7c6065e9cf41f6dc574fcbf956d5e3

v0.3.7
------

- New protocol for listener <=> clients & analyzers <=> alerter  issue#42

v0.3.6
-------

- issue#32 https://github.com/eleme/node-bell/issues/32
   - add comman used client
   - export statsd as `node-bell/upstream/statsd`

v0.3.5
------

- default timer type 'upper_90' => 'mean_90'
- minor fixes (including css, typo..)

v0.3.4
------

- add new service cleaner, issue#29
- trending with time relatived, issue#30

v0.3.3
------

- remove `trending values` support, new trending: z-score + wma
- add option `stop` to webapp
- multi can be negative values now
- trending up/down in alerter
- simple loader gif to webapp

v0.3.2
------

- make `analyzer.filter` async, analyzer is faster
- switch logging library from @TJ log.js to bunyan.
- analyzers/webapp cluster how to in faq.md
- trending: using `wma & zset`, no more `hash` or `zcount`
- ability to see history data
- rebuild alerter, using ssdb `setx`
