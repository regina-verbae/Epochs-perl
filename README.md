# Epochs
Convert various epoch times to `Time::Moment` times in Perl.

For example, running this code

```perl
#!/usr/bin/env perl

use v5.10;
use strict;
use warnings;
use Epochs;

say Epochs::unix(1234567890);

say Epochs::chrome(12879041490654321);
```

would give

```
2009-02-13T23:31:30Z
2009-02-13T23:31:30.654321Z
```

**Update:** Now there are functions in the other direction too! For example, running this

```perl
#!/usr/bin/env perl

use v5.10;
use strict;
use warnings;
use Epochs;

say Epochs::to_unix('2009-02-13T23:31:30Z');

say Epochs::to_chrome('2009-02-13T23:31:30.654321Z');
```

gives

```
1234567890
12879041490654321
```

## Contributors

[@noppers](https://github.com/noppers) originally worked out how to do the Google Calendar calculation.

## History

This project was first done with [DateTime](http://p3rl.org/DateTime). Then it was refactored to use [Time::Piece](http://p3rl.org/Time::Piece), which is in the standard library. When I found out about [Time::Moment](http://p3rl.org/Time::Moment), I just had to refactor it again. Dependencies be damned-- I like this one the best!

## See Also

See [epochs](https://github.com/oylenshpeegul/epochs) for a similar
thing in Go.

See [Epoch-elixir](https://github.com/oylenshpeegul/Epochs-elixir) for a similar
thing in Elixir.

See [the Epochs gh-page](http://oylenshpeegul.github.io/Epochs-perl/) for motivation.
