# Makefile
#
# {{cookiecutter.name}}
# {{cookiecutter.email}}
# (c) {{cookiecutter.affiliation}}
#
# {{cookiecutter.date}}
#

.PHONY = dry_run run

dry_run:
	@snakemake -npr --jn "snakejob.{jobid}" -j 999  --keep-going --rerun-incomplete \
		--snakefile src/Snakefile \
		--configfile config/config.yaml

run:
	@snakemake --jn "snakejob.{jobid}" -j 999  --keep-going --rerun-incomplete \
		--snakefile src/Snakefile \
		--configfile config/config.yaml \
		--cluster-config config/cluster.yaml \
		--cluster "sbatch --output {cluster.output} --time {cluster.time} --mem {cluster.mem}" \
		&> logs/snakemake.log&
