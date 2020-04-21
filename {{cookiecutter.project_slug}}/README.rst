{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}
{% for _ in cookiecutter.project_name %}={% endfor %}
{{ cookiecutter.project_name }}
{% for _ in cookiecutter.project_name %}={% endfor %}

.. start-badges

.. list-table::
    :stub-columns: 1

    * - build
      - |travis|
    * - quality
      - |codacy| |codeclimate| |sonar-qg| |sonar-rel|
    * - coverage
      - |coveralls| |codecov| |codeclimate-cov|
    * - dependencies
      - |pyup| |pyup-p3| |requires|


.. |travis| image:: https://api.travis-ci.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}.svg
   :target: https://travis-ci.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}
   :alt: Travis Build Status

.. |codacy| image:: https://api.codacy.com/project/badge/Grade/CODACY_ID
   :target: https://www.codacy.com/manual/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}
   :alt: Codacy Grade

.. |codeclimate| image:: https://api.codeclimate.com/v1/badges/CODECLIMATE_ID/maintainability
   :target: https://codeclimate.com/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/maintainability
   :alt: Code Climate Maintainability

.. |sonar-qg| image:: https://sonarcloud.io/api/project_badges/measure?project={{ cookiecutter.github_username }}_{{ cookiecutter.project_slug }}&metric=alert_status
   :target: https://sonarcloud.io/dashboard?id={{ cookiecutter.github_username }}_{{ cookiecutter.project_slug }}
   :alt: Sonar Quality Gate Status

.. |sonar-rel| image:: https://sonarcloud.io/api/project_badges/measure?project={{ cookiecutter.github_username }}_{{ cookiecutter.project_slug }}&metric=reliability_rating
   :target: https://sonarcloud.io/dashboard?id={{ cookiecutter.github_username }}_{{ cookiecutter.project_slug }}
   :alt: Sonar Reliability Rating

.. |coveralls| image:: https://coveralls.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/badge.svg?branch=master
   :target: https://coveralls.io/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}?branch=master
   :alt: Coveralls Test Coverage

.. |codecov| image:: https://codecov.io/gh/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/branch/master/graph/badge.svg
   :target: https://codecov.io/gh/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}
   :alt: CodeCov

.. |codeclimate-cov| image:: https://api.codeclimate.com/v1/badges/CODECLIMATE_ID/test_coverage
   :target: https://codeclimate.com/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/test_coverage
   :alt: Code Climate Test Coverage

.. |pyup| image:: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/shield.svg
   :target: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/
   :alt: Updates

.. |pyup-p3| image:: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/python-3-shield.svg
   :target: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/
   :alt: Python 3

.. |requires| image:: https://requires.io/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/requirements.svg?branch=master
   :target: https://requires.io/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/requirements/?branch=master
   :alt: Requirements Status

.. end-badges




{{ cookiecutter.project_short_description }}

{% if is_open_source %}
* Free software: {{ cookiecutter.open_source_license }}
* Documentation: https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io.
{% endif %}

Features
--------

* TODO

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
