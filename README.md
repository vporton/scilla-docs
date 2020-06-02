# Scilla Docs

Scilla short for Smart Contract Intermediate-Level LAnguage is a smart contract
language being developed for Zilliqa.

## Contributing

If you spot any issues or have any ideas on how we can improve the
documentation, help us log an issue
[here](https://github.com/Zilliqa/scilla-docs/issues)

## Installing dependencies

To compile the documentation you need the following dependencies.

1. You need to have [sphinx](http://www.sphinx-doc.org/en/master/) installed.
   Install Sphinx by running `pip install -U Sphinx`.
2. Our build system checks for spelling mistakes automatically (we use the UK
   spelling, by the way). To enable it some additional dependencies are needed.
   - The [sphinxcontrib.spelling][spelling] spelling cheker for Sphinx:
   `pip install -U sphinxcontrib-spelling`.
   - The command above will automatically install [PyEnchant][pyenchant] library
     which itself needs the C [Enchant][enchant] library which one has to
     install using e.g. your OS's package manager. You can find the installation
     instructions [here][enchant-install]. Basically, you want either
     `libenchant` or `enchant` package depending on your setup.

[spelling]: https://sphinxcontrib-spelling.readthedocs.io/en/latest/index.html
[pyenchant]: https://pyenchant.github.io/pyenchant/index.html
[enchant]: https://www.abisource.com/projects/enchant/
[enchant-install]: https://pyenchant.github.io/pyenchant/install.html#installing-the-enchant-c-library
   
## Building the docs
   
Run `make html` from [docs](./docs/) folder and make sure that the edits are rendered
correctly on the HTML files.

If you need to teach the spelling checker more words, add them to the
[spelling_wordlist.txt](./docs/source/spelling_wordlist.txt) file. The format is
really simple -- it's just one word per line the file. And the file is sorted in
ascending order.

### Before submitting a pull request

Please preview your HTML files _before_ submitting a pull request. Try to
[squash](https://blog.github.com/2016-04-01-squash-your-commits/) your commits
before making the pull request. We know it's difficult, but it helps us keep our
commit logs clean and makes the reviewers' lives easier.

