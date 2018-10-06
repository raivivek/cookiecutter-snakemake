## Snakemake (cookiecutter)

Repository provides a _cookiecutter_ template for Snakemake driven analysis.
The organization and use case is inspired by Snakemake's heavy use in
Bioinformatics analysis, but feel free to adapt it for your personal use.

## Usage

Install `cookiecutter` and initialize project (with desired details):

```
pip install cookiecutter
cookiecutter https://github.com/raivivek/snakemake-cookiecutter
```

## Try it

```
$ make dry_run

localrule all:
  jobid: 0
  reason: Rules with neither input nor output files are always executed.

Job counts:
  count   jobs
  1       all
  1
```

## Details

```
{{cookiecutter.project_slug}}
├── bin
├── config
│   ├── cluster.yaml
│   └── config.yaml
├── logs
├── Makefile
├── README.md
└── src
    └── Snakefile
```

## License

See [LICENSE](./LICENSE).
