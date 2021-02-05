# Build & publish

Build & publish to Azure

1. Install Twine and the keyring

    pip install twine keyring artifacts-keyring

2. Add a .pypirc to your home directory

    [distutils]
    Index-servers =
    Distro

    [Distro]
    Repository = https://pkgs.dev.azure.com/borregaard/d33303bb-c3fe-4b1f-9c0a-091ad1832a5d/_packaging/Distro/pypi/upload

3. Publish packages

    python setup.py sdist bdist_wheel

    twine upload -r Distro dist/*