{% set is_open_source = cookiecutter.license != 'Proprietary' -%}
# {{ cookiecutter.project_name }}

{{ cookiecutter.project_short_description }}

{% if is_open_source %}
* Free software: {{ cookiecutter.license }}
* Documentation: https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io.
{% endif %}

# Features

* TODO

# Credits

This package was created with Cookiecutter and the Aicura custom component package template.
 - Cookiecutter: https://github.com/audreyr/cookiecutter