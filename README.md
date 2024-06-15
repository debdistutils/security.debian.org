# Git LFS mirror of `security.debian.org`

This git repository contains a mirror of
[security.debian.org](https://security.debian.org/), with external
objects stored using [Git LFS](https://git-lfs.com/).

This repository was created using rsync from [the
`debian.snt.utwente.nl` mirror of
security.debian.org](https://www.debian.org/CD/mirroring/rsync-mirrors)
on 2024-04-30.  The goal is to keep it in sync with
`security.debian.org` going forward.

## Cloning

The Git LFS objects are not available via GitLab, therefor to clone
this repository successfully you will need to disable Git LFS smudging
using the `GIT_LFS_SKIP_SMUDGE=1` environment variable like this:

```
GIT_LFS_SKIP_SMUDGE=1 git clone https://gitlab.com/debdistutils/archives/debian/security.debian.org.git
```

# Signature Verification

Commits are signed using [my PGP
key](https://blog.josefsson.org/2019/03/21/openpgp-2019-key-transition-statement/)
with fingerprint:

```
pub   ed25519 2019-03-20 [SC]
      B1D2 BD13 75BE CB78 4CF4  F8C4 D73C F638 C53C 06BE
```

Alternatively, the new dedicated importer key with the following
fingerprint:

```
sec   rsa3072 2024-06-15 [SC]
      A6DB 3F7E A841 C2E2 1D5E  72A1 0BC2 D729 80EC B489
uid   Apt archive Git LFS importer <apt2gitlfs@snapt.debian.net>
```

You may view git log and verify commit signatures them as follows:

```
git log --show-signature
```

To verify a single commit use something like this:

```
$ git verify-commit d125d6f58438b0f5c0613319eee1c7098d97abbd
gpg: Signature made Tue Apr 30 14:19:55 2024 CEST
gpg:                using EDDSA key A3CC9C870B9D310ABAD4CF2F51722B08FE4745A2
gpg: Good signature from "Simon Josefsson <simon@josefsson.org>" [ultimate]
$ 
```

## Contact

The maintainer is [Simon Josefsson](https://blog.josefsson.org/).
