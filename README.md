# lambdacd-cron

A cron trigger for your [LambdaCD](https://github.com/flosell/lambdacd).

## Status

[![Build Status](https://travis-ci.org/felixb/lambdacd-cron.svg?branch=master)](https://travis-ci.org/felixb/lambdacd-cron)

[![Clojars Project](https://clojars.org/lambdacd-cron/latest-version.svg)](https://clojars.org/lambdacd-cron)

## Usage

In project.clj add
```clojure
:dependencies [[lambdacd-cron "<most recent version>"]]
```

Add the following code to your import statements of your pipeline code
```clojure
(:require [lambdacd-cron.core :as lambdacd-cron])
```

The following code adds a step to your pipeline which triggers every day at 12:00 UTC
```clojure
(lambdacd-cron/cron "0 12 * * *")
```

You'll find a complete example here: [example/pipeline.clj](https://github.com/felixb/lambdacd-cron/blob/master/example/lambdacd_cron/example/pipeline.clj)

## Supported cron patterns

The cron pattern given to `(cron)` consists of the following parts:
* minutes
* hours
* day-of-month
* month
* day-of-week

## Contributing

Feel free to propose any change by sending a PR.

## License

Copyright © 2016 Felix Bechstein

Distributed under the Apache License 2.0
