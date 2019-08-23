# KCov Backport for Linux 3.10.108

This repository contains a working KCov backport for Linux v3.10.108. In other words, it's generated as follows:

```bash
git diff v3.10.108 > kcov.diff
```

## Usage

To apply the patch, use the following commands inside the [kernel repository]:

```bash
git checkout v3.10.108
git apply /path/to/kcov.diff
```

Additionally, it contains a `Kconfig` file ready to use with [syzkaller].

## License

The backport is implemented by Mingzhe Wang, and licensed under GPLv2. It's an artifact of [our paper] in ESEC/FSE 2019. When using the backport for a publication, please cite as follows:

```
@inproceedings{shi2019industry,
 author = {Shi, Heyuan and Wang, Runzhe and Fu, Ying and Wang, Mingzhe and Shi, Xiaohai and Jiao, Xun and Song, Houbing and Jiang, Yu and Sun, Jiaguang},
 title = {Industry Practice of Coverage-guided Enterprise Linux Kernel Fuzzing},
 booktitle = {Proceedings of the 2019 27th ACM Joint Meeting on European Software Engineering Conference and Symposium on the Foundations of Software Engineering},
 series = {ESEC/FSE 2019},
 year = {2019},
 isbn = {978-1-4503-5572-8},
 location = {Tallinn, Estonia},
 pages = {986--995},
 numpages = {10},
 url = {http://doi.acm.org/10.1145/3338906.3340460},
 doi = {10.1145/3338906.3340460},
 acmid = {3340460},
 publisher = {ACM},
 address = {New York, NY, USA},
 keywords = {Kernel fuzzing, bug detection, enterprise Linux},
} 
```

[syzkaller]: https://github.com/google/syzkaller
[our paper]: http://www.wingtecher.com/themes/WingTecherResearch/assets/papers/fse19-linux-kernel.pdf
[kernel repository]: https://github.com/torvalds/linux/
