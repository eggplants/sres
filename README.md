# `sres`

## Requirement

- [Sublist3r](https://github.com/aboul3la/Sublist3r)

```bash
$ git clone https://github.com/aboul3la/Sublist3r && cd Sublist3r
$ pip install -e .
```

- curl

```bash
$ sudo apt install curl
```

## Install

- Local

```bash
$ mkdir -p sres && cd sres
$ wget -nv https://raw.githubusercontent.com/eggplants/sres/master/sres
$ chmod +x sres
```

- Global

```bash
$ wget -nv https://raw.githubusercontent.com/eggplants/sres/master/sres
$ sudo install -m 0755 echo-sd /usr/local/bin/sres
$ rm sres
```

## Run

- See: `example` - the result of checking `example.com` and `tsukuba.ac.jp`

```bash
$ ./sres tsukuba.ac.jp # Ctrl - C to abort
Created: tsukuba_ac_jp-20210326-032546.txt, tsukuba_ac_jp-20210326-032546_res.csv
```
```bash
$ head tsukuba*.txt # list of subdomains
```

```text
www.tsukuba.ac.jp
16.13.tsukuba.ac.jp
17.13.tsukuba.ac.jp
18.13.tsukuba.ac.jp
32.13.tsukuba.ac.jp
1.237.tsukuba.ac.jp
100.237.tsukuba.ac.jp
16.237.tsukuba.ac.jp
32.237.tsukuba.ac.jp
193.244.tsukuba.ac.jp
```

```bash
$ head tsukuba*_res.csv # http response list of subdomains
```

```csv
url,res_code,content_type,res_time,redirect_url
1.237.tsukuba.ac.jp,000,,0.000000s,
1.250.tc.tsukuba.ac.jp,000,,0.000000s,
100.237.tsukuba.ac.jp,000,,0.000000s,
103-41-62-10.takoi.softlab.cs.tsukuba.ac.jp,000,,0.000000s,
103-41-62-11.takoi.softlab.cs.tsukuba.ac.jp,000,,0.000000s,
103-41-62-12.takoi.softlab.cs.tsukuba.ac.jp,000,,0.000000s,
103-41-62-13.takoi.softlab.cs.tsukuba.ac.jp,000,,0.000000s,
103-41-62-15.takoi.softlab.cs.tsukuba.ac.jp,000,,0.000000s,
103-41-62-8.takoi.softlab.cs.tsukuba.ac.jp,000,,0.000000s,
```

- Create: `res_{200,301}.csv`

```bash
$ (sed 1\!d tsukuba*_res.csv;grep ',200,' tsukuba*_res.csv) | cut -d, -f5 --complement > res_200.csv
$ (sed 1\!d tsukuba*_res.csv;grep ',301,' tsukuba*_res.csv) > res_301.csv
```
