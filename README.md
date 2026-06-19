https://github.com/lxyeternal/pypi_malregistry
https://github.com/DataDog/malicious-software-packages-dataset

Analysis command (dry run)

```
docker run --cgroupns=host --privileged --rm -ti -v /var/lib/containers:/var/lib/containers -v /tmp/1inch/results:/results -v /tmp/1inch/staticResults:/staticResults -v /tmp/1inch/writeResults:/writeResults -v /tmp/1inch/dockertmp:/tmp -v /tmp/1inch/analyzedPackages:/analyzedPackages -v /tmp/1inch/straceLogs:/straceLogs -v /home/atharva/programs/supplychain/package-analysis/data/1inch-8.6.tar.gz:/1inch-8.6.tar.gz gcr.io/ossf-malware-analysis/analysis analyze -dynamic-bucket file:///results/ -file-writes-bucket file:///writeResults/ -static-bucket file:///staticResults/ -analyzed-pkg-bucket file:///analyzedPackages/ -execution-log-bucket file:///results -ecosystem pypi -package 1inch -local /1inch-8.6.tar.gz
```
