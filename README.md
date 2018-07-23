### weepushover

`weepushover` is a WeeChat plugin written in Python to send push notifications from WeeChat to Pushover. The plugin requires you to create an application token (`token`) and an user token (`user`) before you can use it.

#### Settings

Prefix each setting with `plugins.var.python.weepushover.<setting>`:

```
token                 your application token (required)
user                  your user token (required)
ignored_channels      space-separated list of channels to ignore
subscribed_channels   space-separated list of channels to subscribe to
away_only             send only when marked as away
inactive_only         send only when the message is in an inactive buffer
min_notify_interval   minimum number of seconds to wait before another notification
debug                 print debug messages in core
```

For example, if I wanted to set the `token` setting, I'd do:

```
/set plugins.var.python.weepushover.token azGDORePK8gMaC0QOYAMyEEuzJnyUi
```

#### Credits

The original inspiration for this script was from LeftyBC's [`weebullet.py`](https://github.com/LeftyBC/weebullet).

#### What's different?

Yes, there are other Pushover plugins (see [`pushover.pl`](https://weechat.org/scripts/source/pushover.pl.html/) and [`pushover-weechat.rb`](https://github.com/jamtur01/pushover-weechat) for WeeChat. However, I chose to write my own because none of them had the `subscribe` feature: I'm a part of a low-traffic channel in which I'd like to receive a notification for *all* messages, irrespective of whether or not I'm highlighted.

I could have added the feature in the other two plugins, but I don't know Ruby and Perl that well. Plus, this way, I have complete control over features in the plugin.

#### License

```
Copyright 2018 Commento, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
