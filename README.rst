Feedfinder2
===========

This is a Python library for finding links feeds on a website. It is based on
`feedfinder <http://www.aaronsw.com/2002/feedfinder/>`_ - originally
written by `Mark
Pilgrim <http://en.wikipedia.org/wiki/Mark_Pilgrim_(software_developer)>`_ and
subsequently maintained by `Aaron
Swartz <http://en.wikipedia.org/wiki/Aaron_Swartz>`_ until his untimely death.

Usage
-----

Feedfinder2 offers a single public function: ``find_feeds``. You would use it
as follows:

::

    import asyncio

    from feedfinder2 import find_feeds


    async def main():
        feeds = await find_feeds("cnews.ru/")
        print(feeds)


    if __name__ == "__main__":
        asyncio.run(main())

Now, ``feeds`` is the list: ``['http://xkcd.com/atom.xml',
'http://xkcd.com/rss.xml']``. There is some attempt made to rank feeds from
best candidate to worst but... well... you never know.

License
-------

Feedfinder2 is licensed under the MIT license (see LICENSE).
