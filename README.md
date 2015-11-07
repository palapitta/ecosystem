We, the module installer developers, hereby decree...

Too official? Ok, I'll go again.

In this repository you'll find metadata for projects and modules. It's nice
to have that in a central place, apart from any specific module installer
(*cough* proto neutro pls *cough*), for at least these three reasons:

* The set of people who want access to a module installer and the set of
  people who want access to module metadata are two different sets.

* If each installer has one set of metadata, that's more for everyone to
  keep updated. If it's in a central place, there's less work.

* The list of projects in the ecosystem is really an orthogonal to the
  installer, or even *an* installer. It might be used for other things,
  such as rendering the list at http://modules.perl6.org

To add a new module to the ecosystem, add the URL of the module's raw META.info
file to the META.list file here in the ecosystem. Since the updates to
the ecosystem are announced in the #perl6 IRC channel, it is helpful
if you include the HTTP URL to your repo in your commit message, so others
could easily view your new module, e.g.:

    git commit -m 'Add FooBar to ecosystem' -m 'See https://github.com/foobar/FooBar'

So there you go. It probably bears repeating that all of this is quite
temporary; something to sustain us until we can hook up with CPAN goodness
in some more long-term way.

Have a nice day.

### Common Errors

Some of these issues commonly occur. Be sure to check your distro:

* Either `git://` or `https://` source URL will work, but:
    * If using `git://`, be sure your URL ends with `.git`
    * If using `https://`, be sure your URL ends with a `/`

* Check that your META file contains valid JSON. To do so, you can use an online service, such as [JSON Lint](http://jsonlint.com/).
