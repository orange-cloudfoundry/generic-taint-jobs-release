# BOSH release for generic-bosh-deployment-taint-jobs

This BOSH release and deployment manifest deploy a cluster of generic-bosh-deployment-taint-jobs.

## Usage

This repository includes base manifests and operator files. They can be used for initial deployments and subsequently used for updating your deployments:

```plain
export BOSH_ENVIRONMENT=<bosh-alias>
export BOSH_DEPLOYMENT=generic-bosh-deployment-taint-jobs
git clone https://github.com/cloudfoundry-community/generic-bosh-deployment-taint-jobs-boshrelease.git
bosh deploy generic-bosh-deployment-taint-jobs-boshrelease/manifests/generic-bosh-deployment-taint-jobs.yml
```

If your BOSH does not have Credhub/Config Server, then remember `--vars-store` to allow generation of passwords and certificates.

### Update

When new versions of `generic-bosh-deployment-taint-jobs-boshrelease` are released the `manifests/generic-bosh-deployment-taint-jobs.yml` file will be updated. This means you can easily `git pull` and `bosh deploy` to upgrade.

```plain
export BOSH_ENVIRONMENT=<bosh-alias>
export BOSH_DEPLOYMENT=generic-bosh-deployment-taint-jobs
cd generic-bosh-deployment-taint-jobs-boshrelease
git pull
cd -
bosh deploy generic-bosh-deployment-taint-jobs-boshrelease/manifests/generic-bosh-deployment-taint-jobs.yml
```
