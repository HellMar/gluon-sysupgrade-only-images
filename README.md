# Bauanleitung für UBNT-ERX Factory-Images mit Gluon-v2020.1 als Basis

```
git clone https://github.com/freifunk-gluon/gluon.git 
cd gluon
git checkout -b v2020.1.2
git clone git@github.com:HellMar/gluon-sysupgrade-only-images.git
git am site/patches/0001-added-TP-Link-TL-WR841ND-N-Devices-for-8M-and-16M.patch
make update
make -j8 GLUON_TARGET="ar71xx-generic" GLUON_DEVICES="tp-link-tl-wr841n-nd-mod-8m-v8 tp-link-tl-wr841n-nd-mod-8m-v9 tp-link-tl-wr841n-nd-mod-8m-v10 tp-link-tl-wr841n-nd-mod-8m-v11 tp-link-tl-wr841n-nd-mod-16m-v8 tp-link-tl-wr841n-nd-mod-16m-v9 tp-link-tl-wr841n-nd-mod-16m-v10 tp-link-tl-wr841n-nd-mod-16m-v11" GLUON_RELEASE="GenericFactoryImage-v0.1_Gluon-v2020.1.2"

```

