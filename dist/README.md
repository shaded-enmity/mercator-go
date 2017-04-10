# Dist files for Mercator Go

## How to build Mercator Go for OpenShift

1. Clone the repo from https://github.com/baytemp/mercator-go.git 
2. Go to the cloned repo dir and build `mercator` by running (follow the instructions from https://github.com/baytemp/mercator-go):

   ```sh
$ make build  # probably you would like to specify `GOPATH` environment variable as well
   ```

3. Enter `dist` dir and run `./build-for-openshift.sh` (uses `mercator-for-openshift.spec` specfile). Make sure you have enabled ecosystems that you want to use in `mercator-for-openshift.spec` (in the `%install` section).
4. Use your source RPM at https://copr.devel.redhat.com/coprs/fpokorny/mercator-go. Do not use podvody/mercator-go as we use it in Bayesian development.
