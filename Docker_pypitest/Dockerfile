FROM python:3

COPY . /altility
WORKDIR /altility

RUN python3 -m pip install --upgrade twine build

RUN python3 -m build

CMD python3 -m twine upload --config-file .pypirc_test --repository testpypi dist/* \
    && python3 -m pip install -i https://test.pypi.org/simple/ altility
