# workflows

## Using Athena (local VM)
````
$ docker pull atlas/centos7-atlasos
$ su -c "setenforce 0"
$ docker run -i -t -v /cvmfs:/cvmfs atlas/centos7-atlasos /bin/bash
$ yum update
$ yum install voms-clients-cpp man-db
$ wget https://bootstrap.pypa.io/pip/2.7/get-pip.py
$ python get-pip.py
$ git clone https://github.com/PanDAWMS/panda-client.git
$ git checkout snakemake_workflows
$ pip install .
$ https://github.com/retmas-dv/workflows.git
$ cd ~/workflows
$ export ATLAS_LOCAL_ROOT_BASE=/cvmfs/atlas.cern.ch/repo/ATLASLocalRootBase
$ alias setupATLAS='source ${ATLAS_LOCAL_ROOT_BASE}/user/atlasLocalSetup.sh'
$ setupATLAS
$ asetup AthGeneration,21.6.92
$ pchain --useAthenaPackages --intrSrv -v --snakefile ./activelearning/sequential_loop/Snakefile --outDS user.retmas.d3237e41-4657-4bf5-95f0-a0f7b51b3c4e
````