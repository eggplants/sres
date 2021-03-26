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

- Grobal

```bash
$ wget -nv https://raw.githubusercontent.com/eggplants/sres/master/sres
$ sudo install -m 0755 echo-sd /usr/local/bin/sres
$ rm sres
```

## Run

- See: `example` - the result of checking `example.com` and `tsukuba.ac.jp`

```bash
$ ./sres <domain name>
Created: xxxx-YYYYMMDD-hhmmss.txt, xxxx-YYYYMMDD-hhmmss_res.csv
$ head xxxx-YYYYMMDD-hhmmss.txt # list of subdomains
xxx.xxxxxxx.xx.xx
xx.xx.xxxxxxx.xx.xx
xx.xx.xxxxxxx.xx.xx
xx.xx.xxxxxxx.xx.xx
xx.xx.xxxxxxx.xx.xx
x.xxx.xxxxxxx.xx.xx
xxx.xxx.xxxxxxx.xx.xx
xx.xxx.xxxxxxx.xx.xx
xx.xxx.xxxxxxx.xx.xx
xxx.xxx.xxxxxxx.xx.xx
$ head xxxx-YYYYMMDD-hhmmss_res.csv # response list of subdomains
url,res_code,content_type,res_time,redirect_url
xxx,xxx_xxxx,xxxxxxx_xxxx,xxx_xxxx,xxxxxxxx_xxx
x.xxx.xxxxxxx.xx.xx,xxx,,x.xxxxxxx,
x.xxx.xx.xxxxxxx.xx.xx,xxx,,x.xxxxxxx,
xxx.xxx.xxxxxxx.xx.xx,xxx,,x.xxxxxxx,
xxx-xx-xx-xx.xxxxx.xxxxxxx.xx.xxxxxxx.xx.xx,xxx,,x.xxxxxxx,
xxx-xx-xx-xx.xxxxx.xxxxxxx.xx.xxxxxxx.xx.xx,xxx,,x.xxxxxxx,
xxx-xx-xx-xx.xxxxx.xxxxxxx.xx.xxxxxxx.xx.xx,xxx,,x.xxxxxxx,
xxx-xx-xx-xx.xxxxx.xxxxxxx.xx.xxxxxxx.xx.xx,xxx,,x.xxxxxxx,
xxx-xx-xx-xx.xxxxx.xxxxxxx.xx.xxxxxxx.xx.xx,xxx,,x.xxxxxxx,
```
