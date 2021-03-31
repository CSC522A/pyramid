pyramid_blogr
=============

Getting Started
---------------

- Change directory into your newly created project.

    cd pyramid_blogr

- Create a Python virtual environment.

    python3 -m venv env

- Upgrade packaging tools.

    env/bin/pip install --upgrade pip setuptools

- Change directory to the main file

    cd pyramid_blogr_master

- Install the project in editable mode with its testing requirements.

    pyramid_blogr/env/bin/pip install -e ".[testing]"

- Initialize and upgrade the database using Alembic.

    - Generate your first revision.

        pyramid_blogr/env/bin/alembic -c development.ini revision --autogenerate -m "init"

    - Upgrade to that revision.

        pyramid_blogr/env/bin/alembic -c development.ini upgrade head

- Load default data into the database using a script.

    pyramid_blogr/env/bin/initialize_pyramid_blogr_db development.ini

- Run your project's tests.

    pyramid_blogr/env/bin/pytest

- Run your project.

    pyramid_blogr/env/bin/pserve development.ini
