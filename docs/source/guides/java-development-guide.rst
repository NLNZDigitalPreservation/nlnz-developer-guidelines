======================
Java Development Guide
======================


Introduction
============

This guide, designed for a National Library of New Zealand (NLNZ) (https://natlib.govt.nz/) developer and contributor,
covers how to develop and contribute to NLNZ software projects for code written in the Java development language. It
also covers development in the Groovy language, which is a derivative of Java.

Contents of this document
-------------------------

Following this introduction, the Java Development Guide includes the following sections:

-   **Building** - Covers building jars from source.


Building
========

Requirements
------------

Build requirements for Java projects
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Building a java-based project from source requires the following:

-   Java 11 JDK or above (64bit recommended). Current development assumes the use of OpenJDK.

-   Git (required to clone the project source from Github).

-   Access to maven central either directly or through a proxy.

As the artifact targets are Java-based, it should be possible to build the artifacts on either Linux, Solaris or Windows
targets.

Build requirements for Groovy projects
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Building a java-based project from source requires the following:

-   Java 11 JDK or above (64bit recommended). Current development assumes the use of OpenJDK.

-   Gradle 5.2.1 or later.

-   Groovy 2.5.4 or later.

-   Git (required to clone the project source from Github).

-   Access to maven central either directly or through a proxy.

As the artifact targets are Java-based, it should be possible to build the artifacts on either Linux, Solaris or Windows
targets.

Development platforms
~~~~~~~~~~~~~~~~~~~~~
The following platforms have been used during the development of Java-based projects:

-  Ubuntu GNU/Linux 18.04 LTS and later


Installation
------------
The artifacts are built using gradle and will deploy to a maven repository when various gradle publishing options are
used.

Build commands for Maven-based projects
---------------------------------------

TODO Cover Maven commands.

Build commands for Gradle-based projects
----------------------------------------

Generate API reference::

    gradle javadoc


Building with unit tests
~~~~~~~~~~~~~~~~~~~~~~~~
Unit tests are normally run as part of a build. To explicitly run unit tests::

    gradle [clean] test


Building with unit tests and publishing artifact
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
This can be run from the root project folder::

    gradle [clean] build publishToMavenLocal


Complete build with upgrade-preparation warnings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
When gradle 5.x is released, some gradle features and certain build scripts will not work. In order to prepare for
this eventuality, builds can include the `warning-mode` to notify in advance of changes that will need to happen::

    gradle [clean] build --warning-mode all


Building and skipping unit tests
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Generally unit tests should not be skipped::

    gradle [clean] build -x test


Jacoco code coverage
~~~~~~~~~~~~~~~~~~~~
While the jacoco plugin is included in builds, there isn't currently any tasks associated with jacoco.
TODO Add jacoco code coverage tasks.

check
~~~~~
Run both findBugs and PMD source code analyzer::

    gradle check


findBugs
~~~~~~~~
Normally `gradle check` will only run a findBugs report on the main portion of the source code. findBugs can also run on the test code::

    gradle findBugsMain
    gradle findBugsTest

PMD source code analyzer
~~~~~~~~~~~~~~~~~~~~~~~~
Normally `gradle check` will only run a PMD report on the main portion of the source code. PMD can also run on the test code::

    gradle pmdMain
    gradle pmdTest


