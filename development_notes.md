# Notes for developers

Tests should be run against installed package:

```sh
pip uninstall acachecontrol
rm -rf build
rm -rf dist
python3 setup.py sdist bdist_wheel
pip install --no-cache-dir dist/acachecontrol-{VERSION}.tar.gz
```

Then run tests:
`pytest tests` or `python -m pytest tests`

Supported python versions: 3.6+ (Note that asyncio.run() introduced in 3.7)
