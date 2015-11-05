@title = "Last months' work report"
@author = "Ivan"
@posted_at = '2015-11-06'
@more = true
@preview_image = '/img/pages/road.jpg'
@preview = %(It's been a long time since our last stable release and we have been doing a lot, here is a quick review of the work that has been happening on backstage.)

Last months report
==================

TODO: Make sure that we don't say things that we don't want to communicate to people

It's been 9 months since we released our latest stable version, we have been
working a lot and trying out several release candidates in the way.

We are releasing a new stable Bitmask bundle and along with that we are letting
you all know what's been happening on backstage.

Some numbers
------------

Some numbers on what we have been doing all this time
- we have closed 494 issues,
- we have closed 396 pull requests,
- adding up all the components changes we got 844 new commits,
- in total we have contributions from 26 persons,

You can see the notable ones on our joint changelog for 0.9.0 release:
https://github.com/leapcode/bitmask_client/blob/0.9.0/release-notes.rst


Conferences
-----------

We attended to several conferences:

  - Circumvention Tech Festival (Spain, March 2015)
  - Digital Citizenship and Surveillance Society (Wales, June 2015)
  - Chaos Communication Camp (Germany, August 2015)
  - Tecnologías libres y cooperativas copyleft en el movimiento social de izquierda (Mexico, October 2015)


Funding
-------

TODO: can we write down something for this?


People
------

The usual LEAP team:

Find us on: https://github.com/orgs/leapcode/people

* ThoughtWorks / Pixelated team

We have been working closely with them with platform and Soledad components.

Find them on: https://github.com/orgs/pixelated/people

* Rails GSOC

TODO: elaborate more on this, here we have just some data as a startpoint

The Rails Google Summer Of Code has been a huge success, they worked on the
webapp implementing:
- account disabling and deleting
- invite codes -> already been using on pixelated
- billing

mentors: varac, azul

https://teams.railsgirlssummerofcode.org/teams/90
https://teams.railsgirlssummerofcode.org/teams/52
http://railsgirlssummerofcode.org/blog/2015-09-16-alster-hamburgers-code-review/


* Alireza Mirzaeiyan

Alireza join us for a couple of months to help us build an important missing
piece of Bitmask for Windows. This helped us to get closer to release on that
platform.

Bitmask root service for windows
https://github.com/alirezamirzaeiyan/bitmask-root


Development highlights
----------------------

The main focus of the development since the last release has being on making
bitmask email awesome. There is still a lot of work to do to become the email
service we want to be, but now we already have something to show on how great
bitmask email can become.

We were neglecting our tests battery and we started a process to make all
green, we now have a buildbot instance that runs tests on every commit and
build the (currently provisional) standalone bundle.

We moved towards building bundles using pyinstaller instead of a custom made
bundler scripts, which allows us to easier achieve multiplatform support.

We spent a fair amount of time refactoring our libraries and apps, we aim to
have cleaner and more maintainable code on each iteration, there is still room
to improvement and we will keep working with this in mind on next releases as
well.

We have being working tirelessly into Soledad, our document syncing service
used to sync emails and keys. Soledad now is faster and more stable. All the
API has being redesigned to be asynchronous. The document downloads now are
performed in parallel. And many other parts has being improved. We still have
many great plans for Soledad and a much work ahead, but now is starting to
become the tool we wanted for bitmask.

To be useful our key management needed a lot of rethinking. We've redesign how
we want to discover and manage OpenPGP keys (and maybe others in the future):
https://leap.se/en/docs/design/transitional-key-validation We have a first
working implementation of it in our KeyManager, and we have plans to improve it
step by step to become a hassle free transparent key manager.
