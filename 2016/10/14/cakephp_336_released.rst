CakePHP 3.3.6 Released
======================

The CakePHP core team is happy to announce the immediate availability of CakePHP
3.3.6. This is a maintenance release for the 3.3 branch that fixes several
community reported issues.

Bugfixes
--------

You can expect the following changes in 3.3.6. See the `changelog
<https://github.com/cakephp/cakephp/compare/3.3.5...3.3.6>`_ for every commit.

* The ORM will now correctly handle complex types like datetimes in where
  conditions for associations that are joined with ``joinWith()``, ``innerJoinWith()``,
  ``matching()`` and ``notMatching()``.
* View Cells now include the template and action name when generating cache
  keys. This fixes incorrect cached content from being displayed.
* When autoFields are disabled 1:1 associated records will now be hydrated as an
  empty object.
* The associations generated by BelongsToMany associations now preserve the
  loading strategy defined in the root association.
* A double URL encoding issue on cookie values emitted by the PSR7 HTTP stack.
  This resulted in encrypted cookies not being readable.
* ``TestCase::getMockForModel()`` now correctly sets plugin model aliases.
* ``RoutingMiddleware`` sets the request method based on the ``_method`` request
  data parameter.
* SqlServer handles default values with ``N`` prefixes now.

New Features
------------

* Improved API documentation.
* The ``ajaxLogin`` of ``AuthComponent`` is now deprecated.
* PaginatorHelper supports ``escape => false`` in more methods.
* ``PaginatorHelper::generateUrl()`` was added.
* ``HtmlHelper::meta()`` can now create canonical, next and prev tags.

Contributors to 3.3.6
---------------------

Thank you to all the contributors that helped make this release happen:

* ADmad
* Gareth Ellis
* Hari K T
* Johan Meiring
* Jorge Alberto Cricelli
* José Lorenzo Rodríguez
* Marc Wilhelm
* Marc Ypes
* Mark Story
* Robert Pustułka
* Walther Lalk
* chinpei215
* cjquinn
* dereuromark
* inoas
* phongkt
* saeid
* thinkingmedia

As always, we would like to thank all the contributors that opened issues,
opened pull requests or updated the documentation.

Download a `packaged release on github
<https://github.com/cakephp/cakephp/releases>`_.

.. author:: markstory
.. categories:: release, news
.. tags:: release, news
