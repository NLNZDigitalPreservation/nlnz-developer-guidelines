===============
Developer Guide
===============


Introduction
============

This guide, designed for a National Library of New Zealand (NLNZ) (https://natlib.govt.nz/) developer and contributor,
covers how to develop and contribute to NLNZ software projects.

Contents of this document
-------------------------

Following this introduction, the Developer Guide includes the following sections:

-   **Contributing** - Covers how to contribute to the project.

-   **Language-specific development** - References for language-specific development.

-   **Developer guidelines** - Covers coding practice and development workflow.


Contributing
============

This describes how to contribute to the NLNZ projects.

Source Code Repository
----------------------

Source code for the NLNZ software projects are stored in github at: https://github.com/NLNZDigitalPreservation .
Contributors to the codebase will require a github account.

Issue tracking
--------------

Issues are tracked via Github's issue tracking. The current set of issues can be viewed on the project's *Issues* tab.

When creating issues please include as much information as possible. The more information that you include, the easier
it is for the issue resolver to solve the problem. Useful information includes the following:

Background information
~~~~~~~~~~~~~~~~~~~~~~

-   The version of the NLNZ software you are using

-   The runtime version you are using. For Java programs this would be Java type and version (for example OpenJDK
    8u192). For Python programs it would be the Python version (for example 2.7).

Specific issue information
~~~~~~~~~~~~~~~~~~~~~~~~~~

-   Mention precisely what went wrong, including the steps you took to get to point where things didn't work as
    expected. Describing the steps you took can help us reproduce the issue.

-   Describe what you expected to have happen.

-   Include any relevant log messages.

Pull requests
-------------

Pull requests are managed with Github's pull request process. For pull requests, see the *Pull requests* tab in the
Github project. See :doc:`git-development-guide` for more details.

License
-------

In general, software developed by NLNZ is done under the MIT (2019) License, which can be found at:
https://mit-license.org/

Copyright
---------

In general copyright is assumed to belong to either the person who committed a change or the institution employing that
person.

*Please do not put copyright notices in files.*

Major Contributors
------------------

Major contributors to software development at NLNZ is the National Library of New Zealand itself. The New Zealand
Department of Internal Affairs (DIA) (https://www.dia.govt.nz) also provides software support and assistance. All
contributors are welcome. Making NLNZ aware of your interest in NLNZ software development can help to ensure that the
developed software meets your needs.

Development discussion
----------------------

Currently there are no Slack channels are used to discuss current development, but that may come in the future.

Getting help
------------

If the documentation isn't sufficiently clear, please:
TODO where someone can get help
You can also create github issues for specific problems with the code or its documentation.


Language-specific development
=============================

See :doc:`python-development-guide` and :doc:`java-development-guide` for specific development requirements.


Developer Guidelines
====================

Documentation
-------------

Consider including informative documentation for your project, in the style of this documentation, and hosting it on
https://readthedocs.io . This makes your software more user-friendly and usable.

Coding practice
---------------

-   We assume common good coding practices. Consider following the principles outlined in Robert C. Martin's book
    *Clean Code* (https://www.oreilly.com/library/view/clean-code/9780136083238/ ).

-   New functionality changes have a reasonable set of unit tests included. This can be enforced through minimal code
    coverage tests as part of the build process.

-   Code contains robust instrumentation, which means extensive and detailed logging about the state of operations at
    significant processing points.

Definition of Done
------------------

Code is considered done and can be merged into the master branch when the following conditions have been met:

-   The requirements driving the change have been satisfied by the change.

-   The code builds without errors.

-   All unit tests pass.

-   Unit test code coverage remains the same or is increasing.

-   Functional tests have all passed.

-   Non functional requirements met.

-   Significant user journeys all work.

-   Code and other changes have been peer reviewed and approved.

-   New code has instrumentation (logging points) that conveys accurate and
    helpful information about the state of the application.

-   The documentation has been updated to reflect changes in functionality. Some documents that could be updated
    include:
    -   A *Release Notes* section, especially for new features.
    -   If there are any changes that would require steps to upgrade from a previous version, include an *Upgrade Guide*.
    -   If there is any helpful advice regarding troubleshooting, include a *Troubleshooting Guide*.
    -   If there is helpful information that can be include in a FAQ (Frequently Asked Questions), include a *FAQ*.

-   The Product Owner accepts the changes.

Versioning
----------

See the :doc:`git-development-guide` for a discussion on versioning the code.
