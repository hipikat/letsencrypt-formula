# Changelog

# [3.2.0](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v3.1.0...v3.2.0) (2021-11-18)


### Code Refactoring

* **install:** adapt virtualenv package to OS ([5b92061](https://github.com/saltstack-formulas/letsencrypt-formula/commit/5b920617e89c382059be16c4367a2e15361101ef))
* **install:** change use_package to install_method ([852f110](https://github.com/saltstack-formulas/letsencrypt-formula/commit/852f110df1e72126f517eab48f7475c828025cf5))


### Continuous Integration

* **gemfile+lock:** use `ssf` customised `inspec` repo [skip ci] ([ab94eb5](https://github.com/saltstack-formulas/letsencrypt-formula/commit/ab94eb5d2e8793ed7b2c406cc38aa7b1aa29e6b7))
* **kitchen:** move `provisioner` block & update `run_command` [skip ci] ([65772ab](https://github.com/saltstack-formulas/letsencrypt-formula/commit/65772abcea0c1ade2fdb54449c5810aa4370b421))
* **kitchen+ci:** update with latest `3003.2` pre-salted images [skip ci] ([5aac5bd](https://github.com/saltstack-formulas/letsencrypt-formula/commit/5aac5bd8202adf3a35c5c76aa0b96f4a03dbd9ce))
* **kitchen+ci:** update with latest CVE pre-salted images [skip ci] ([68d6aab](https://github.com/saltstack-formulas/letsencrypt-formula/commit/68d6aab249e87efa1a478b0a919b6b77a090ffd4))
* add Debian 11 Bullseye & update `yamllint` configuration [skip ci] ([46b391d](https://github.com/saltstack-formulas/letsencrypt-formula/commit/46b391d9e161a43efe3a658fbad6a70b53bb250a))
* standardise structure [skip ci] ([650f5e4](https://github.com/saltstack-formulas/letsencrypt-formula/commit/650f5e43a40b8d5328a8abecc6d7ecea29cf2592))


### Documentation

* **readme:** document pip installation method ([288140f](https://github.com/saltstack-formulas/letsencrypt-formula/commit/288140f9c8b17f169fd788dc0aee9964d5b30328))


### Features

* install certbot with pip ([756a272](https://github.com/saltstack-formulas/letsencrypt-formula/commit/756a2722e05dfabc8ad67e502aeef76d0b950018))
* **pip:** allow plugin installation ([ea3b3e0](https://github.com/saltstack-formulas/letsencrypt-formula/commit/ea3b3e04fe5ba3942448839461571e5b202a438a))

# [3.1.0](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v3.0.0...v3.1.0) (2021-07-02)


### Continuous Integration

* **gitlab:** enable `domains` testing on gitlab ([c3637f7](https://github.com/saltstack-formulas/letsencrypt-formula/commit/c3637f7fd1b82469d319b181f0632b3c3b388561))


### Features

* **domains:** allow to specify different authenticators/installers ([87456a1](https://github.com/saltstack-formulas/letsencrypt-formula/commit/87456a1c0601f19e8ce92d7d292b86853abc87cb))

# [3.0.0](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v2.1.1...v3.0.0) (2021-07-02)


### Bug Fixes

* **defaults:** install `certbot` with no plugins ([70dafdd](https://github.com/saltstack-formulas/letsencrypt-formula/commit/70dafdd9456e27d224c94a2bcccc916fedd16bd4))


### Continuous Integration

* **3003.1:** update inc. AlmaLinux, Rocky & `rst-lint` [skip ci] ([f937dca](https://github.com/saltstack-formulas/letsencrypt-formula/commit/f937dca2ff16eff5fc4f855ae2d550ef15eefa34))


### BREAKING CHANGES

* **defaults:** The formula was installing the Apache plugin by default
which is not reasonable. Also, as `letsencrypt:pkgs` is a list,
_adding_ another entry in the list was not replacing this default, causing
undesired packages to be installed.

The new default is an empty list of packages, defaulting to `certbot` in
the code.

## [2.1.1](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v2.1.0...v2.1.1) (2021-06-23)


### Bug Fixes

* **domains:** check cert exists with desired domains ([a11fa8b](https://github.com/saltstack-formulas/letsencrypt-formula/commit/a11fa8b64900598ad1c0845a3fd698feed3c711f)), closes [#57](https://github.com/saltstack-formulas/letsencrypt-formula/issues/57)
* **domains:** update git check cert script ([2cbb50c](https://github.com/saltstack-formulas/letsencrypt-formula/commit/2cbb50c663437a0626237f0a2007d0aa7abd5b1d))
* **gentoo:** use correct `git` package name ([1054e0d](https://github.com/saltstack-formulas/letsencrypt-formula/commit/1054e0db7c67f63ef8fb2967c0c4cb941919fb7a))
* **osfinger:** provide correct package for `centos-7` & `oraclelinux-7` ([19998df](https://github.com/saltstack-formulas/letsencrypt-formula/commit/19998df42d6d9079432ef8e6fc1b766db7ff569b))


### Continuous Integration

* **kitchen+gitlab:** remove Ubuntu 16.04 & Fedora 32 (EOL) [skip ci] ([8b5b4f4](https://github.com/saltstack-formulas/letsencrypt-formula/commit/8b5b4f489aec5d4eab0ad9a0069702ea8f814723))
* add `arch-master` to matrix and update `.travis.yml` [skip ci] ([7ea4e63](https://github.com/saltstack-formulas/letsencrypt-formula/commit/7ea4e63fa226f10be2e0cef6186e83ef2e221e2a))
* **commitlint:** ensure `upstream/master` uses main repo URL [skip ci] ([5def61c](https://github.com/saltstack-formulas/letsencrypt-formula/commit/5def61c38210ca0bcd7bc35dc713d294fb69b40a))
* **gemfile+lock:** use `ssf` customised `kitchen-docker` repo [skip ci] ([8cc1a93](https://github.com/saltstack-formulas/letsencrypt-formula/commit/8cc1a9383fe1b381f7daebc8d55102d476c3ed5f))
* **gitlab-ci:** add `rubocop` linter (with `allow_failure`) [skip ci] ([824c5c2](https://github.com/saltstack-formulas/letsencrypt-formula/commit/824c5c23e65f26c2ec8b72db1657d3a9c9b32d90))
* **gitlab-ci:** use GitLab CI as Travis CI replacement ([90d8a06](https://github.com/saltstack-formulas/letsencrypt-formula/commit/90d8a069b64ded15a5299a0980705cc37a42c069))
* **kitchen+ci:** use latest pre-salted images (after CVE) [skip ci] ([e6c0d13](https://github.com/saltstack-formulas/letsencrypt-formula/commit/e6c0d13ee94cd45c35f9dd1a2eb6bd37a01b2e86))
* **kitchen+gitlab:** adjust matrix to add `3003` [skip ci] ([493ab98](https://github.com/saltstack-formulas/letsencrypt-formula/commit/493ab98f014734d3c5f622f8fbe6bd7a0c01ea10))
* **kitchen+gitlab-ci:** use latest pre-salted images [skip ci] ([ae1610b](https://github.com/saltstack-formulas/letsencrypt-formula/commit/ae1610bd60d82ba3c9a10da1f27d086d89380ef9))
* **pre-commit:** update hook for `rubocop` [skip ci] ([a9cbb16](https://github.com/saltstack-formulas/letsencrypt-formula/commit/a9cbb1650f92042406d3de4f37e0e25567cf10cb))


### Documentation

* **readme:** fix `coala` violations [skip ci] ([98c2898](https://github.com/saltstack-formulas/letsencrypt-formula/commit/98c2898e28f5bd2f45fda395805ce3af4c360228))
* **readme:** stretch is now old-stable [skip ci] ([7f0bab5](https://github.com/saltstack-formulas/letsencrypt-formula/commit/7f0bab5493331fcb66a82baf0b4dd1b91c03856c))


### Tests

* standardise use of `share` suite & `_mapdata` state [skip ci] ([1105cb8](https://github.com/saltstack-formulas/letsencrypt-formula/commit/1105cb896a57ccdf2906ad225e757773686aeceb))

# [2.1.0](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v2.0.0...v2.1.0) (2020-10-26)


### Continuous Integration

* **pre-commit:** add to formula [skip ci] ([0ca8d4f](https://github.com/saltstack-formulas/letsencrypt-formula/commit/0ca8d4f92f721161a2b0de15e882fbf144e1f017))
* **pre-commit:** enable/disable `rstcheck` as relevant [skip ci] ([87e6d43](https://github.com/saltstack-formulas/letsencrypt-formula/commit/87e6d43da34943ae5435615939417b2c251394a9))
* **pre-commit:** finalise `rstcheck` configuration [skip ci] ([30492a3](https://github.com/saltstack-formulas/letsencrypt-formula/commit/30492a36a285baa428b7a3e894246998a5dce8c2))


### Features

* **map:** add `create_init_cert_subcmd` var ([20f9b35](https://github.com/saltstack-formulas/letsencrypt-formula/commit/20f9b35fda19a7bad7335283fc566836a7631ab1))

# [2.0.0](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v1.1.0...v2.0.0) (2020-08-26)


### Code Refactoring

* use domains' setname as --cert-name option ([68fb247](https://github.com/saltstack-formulas/letsencrypt-formula/commit/68fb2475508fea71caf542f62be0e5ce3789e90e))


### BREAKING CHANGES

* Since this domains' setname was not used, the path was named
after the first domain in the domains set. In order to keep using this workflow,
you need to rename the setname with the first domain in the list like the
following:
```
letsencrypt:
  domains:
    foo.example.com:
      - foo.example.com
```

# [1.1.0](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v1.0.0...v1.1.0) (2020-07-29)


### Features

* **map:** add FreeBSD support for certbot ([911a443](https://github.com/saltstack-formulas/letsencrypt-formula/commit/911a443070d601f30a0b43e6dc258fd00a7d70cb))

# [1.0.0](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v0.20.2...v1.0.0) (2020-07-23)


### Bug Fixes

* **package:** amazonlinux defaults to python2 ([926c779](https://github.com/saltstack-formulas/letsencrypt-formula/commit/926c779d477e86ee99eeb435a7bca66b023cf594))
* **server:** change server to ACMEv2 ([1fc79b8](https://github.com/saltstack-formulas/letsencrypt-formula/commit/1fc79b858364d08621dcd2b606e6adf440d0d9f8)), closes [#72](https://github.com/saltstack-formulas/letsencrypt-formula/issues/72)


### Documentation

* **defaults:** update pillar.example to good-citizen defaults ([b889678](https://github.com/saltstack-formulas/letsencrypt-formula/commit/b889678880d89ca629e13551fbd31a5b447b8e16))


### Features

* **config:** add sane defaults ([d9afac9](https://github.com/saltstack-formulas/letsencrypt-formula/commit/d9afac941c17f57b97ca50e70cf78a21e60c39c5))
* **package:** update default to py3 ([4c93c11](https://github.com/saltstack-formulas/letsencrypt-formula/commit/4c93c119d2fd596bfd032598f8f4883ec999b748))


### BREAKING CHANGES

* **config:** `config` can now be provided as a hash or a string; defaults
are modified and, while sane and desirable, do change the behavior of the
formula.

## [0.20.2](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v0.20.1...v0.20.2) (2020-07-07)


### Bug Fixes

* **domains:** renew --no-random-sleep-on-renew ([07cbc3b](https://github.com/saltstack-formulas/letsencrypt-formula/commit/07cbc3bf8877bbca9da067e9208ac7c05d651b00))


### Continuous Integration

* **kitchen:** use `saltimages` Docker Hub where available [skip ci] ([be61a98](https://github.com/saltstack-formulas/letsencrypt-formula/commit/be61a987832218a3b0036c33fec6ccab343b0d86))

## [0.20.1](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v0.20.0...v0.20.1) (2020-06-11)


### Bug Fixes

* **install:** reload after install, to enable salt.modules.acme ([8682b80](https://github.com/saltstack-formulas/letsencrypt-formula/commit/8682b80593a23454a91919cae9c716ce56e4097f))
* **release.config.js:** use full commit hash in commit link [skip ci] ([d9b4559](https://github.com/saltstack-formulas/letsencrypt-formula/commit/d9b45596c629b398be89b4b63cd1af6f6b08404c))


### Continuous Integration

* **gemfile:** restrict `train` gem version until upstream fix [skip ci] ([a965594](https://github.com/saltstack-formulas/letsencrypt-formula/commit/a965594ec9f59ef9caed0a483ed7d40395fb7b5a))
* **gemfile.lock:** add to repo with updated `Gemfile` [skip ci] ([be11444](https://github.com/saltstack-formulas/letsencrypt-formula/commit/be114445aad0db88f0c54dd58fac39d2fafc72fa))
* **kitchen:** avoid using bootstrap for `master` instances [skip ci] ([05afe35](https://github.com/saltstack-formulas/letsencrypt-formula/commit/05afe358e12e828ba1a16c833933238272ff32d0))
* **kitchen:** use `develop` image until `master` is ready (`amazonlinux`) [skip ci] ([c92511b](https://github.com/saltstack-formulas/letsencrypt-formula/commit/c92511b105b8a3f7c27f79b98d60d562923ee2dd))
* **kitchen+travis:** remove `master-py2-arch-base-latest` [skip ci] ([fd89ecb](https://github.com/saltstack-formulas/letsencrypt-formula/commit/fd89ecb28cd4a825c5a7e9d81edbf56b98d6d22f))
* **kitchen+travis:** upgrade matrix after `2019.2.2` release [skip ci] ([60f1a39](https://github.com/saltstack-formulas/letsencrypt-formula/commit/60f1a39c56477b1b40ad3b113a297cad03068fc2))
* **travis:** add notifications => zulip [skip ci] ([c422541](https://github.com/saltstack-formulas/letsencrypt-formula/commit/c422541e4c7f0f4d2859e80ff2fcb94234ee3ac8))
* **travis:** apply changes from build config validation [skip ci] ([a786c41](https://github.com/saltstack-formulas/letsencrypt-formula/commit/a786c417e14059ccf228518ff6fa22dc91c145e4))
* **travis:** opt-in to `dpl v2` to complete build config validation [skip ci] ([42643b5](https://github.com/saltstack-formulas/letsencrypt-formula/commit/42643b52271600d4b270e16f2de8e53bb6f3a9f4))
* **workflows/commitlint:** add to repo [skip ci] ([bb62011](https://github.com/saltstack-formulas/letsencrypt-formula/commit/bb62011bea7553976f7c09049e4946610dc072dd))
* workaround issues with newly introduced `amazonlinux-1` [skip ci] ([380f8d6](https://github.com/saltstack-formulas/letsencrypt-formula/commit/380f8d633a197122162442228094d167989c4800))
* **travis:** quote pathspecs used with `git ls-files` [skip ci] ([443e539](https://github.com/saltstack-formulas/letsencrypt-formula/commit/443e539fc1f0eda9e3705dd6eef784088e49bc7e))
* **travis:** run `shellcheck` during lint job [skip ci] ([e3613df](https://github.com/saltstack-formulas/letsencrypt-formula/commit/e3613df1430959129920c04bdafcdec04f927309))
* **travis:** use `major.minor` for `semantic-release` version [skip ci] ([bc5c44c](https://github.com/saltstack-formulas/letsencrypt-formula/commit/bc5c44cfbef9287766e3ac2f5cd07a0ac8da8388))
* **travis:** use build config validation (beta) [skip ci] ([3dc8c72](https://github.com/saltstack-formulas/letsencrypt-formula/commit/3dc8c72c7287301682ccd35d2cb23b91418ead21))


### Performance Improvements

* **travis:** improve `salt-lint` invocation [skip ci] ([85af6ca](https://github.com/saltstack-formulas/letsencrypt-formula/commit/85af6ca4a9555635ce338851014f0dd6719b0482))

# [0.20.0](https://github.com/saltstack-formulas/letsencrypt-formula/compare/v0.19.1...v0.20.0) (2019-10-24)


### Bug Fixes

* **map.jinja:** fix `salt-lint` errors ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/55b3b31))
* **repo:** provide EPEL repo configuration for `amazon-2` ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/25196c8))
* **rubocop:** add fixes using `rubocop --safe-auto-correct` ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/94e8abe))
* **rubocop:** fix remaining errors manually ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/f313483))
* **yamllint:** fix all errors ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/9aaec41))


### Code Refactoring

* **kitchen:** prefer `kitchen.yml` to `.kitchen.yml` ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/950b95d))
* **kitchen:** use `pillar_from_files` throughout ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/65ee41d))


### Continuous Integration

* **kitchen:** remove redundant settings (all covered under the suites) ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/37a3a56))


### Documentation

* **readme:** modify according to standard structure ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/fcaa79c))
* **readme:** move to `docs/` directory ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/550b56d))


### Features

* **semantic-release:** implement for this formula ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/1a6c486))


### Tests

* **inspec:** fix typo in `git` test filename ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/83f1cac))
* **inspec:** move tests to relevant `controls` sub-directory ([](https://github.com/saltstack-formulas/letsencrypt-formula/commit/71bd8c1))
