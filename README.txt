pyoptools ISO: live CD of Ubuntu with pyoptools

ISO need to be splited for git repository,
also ISO need to be repacked using uncompress procedure below
before being burned to CD-R 
or used in a virtual machine.

#uncompress
cat pyoptools.iso_gz_partN* | gunzip -c > pyoptools.iso



#split and compress: create files less than 100MB
gzip -c  pyoptools.iso | split -b 96MiB - pyoptools.iso_gz_partN
