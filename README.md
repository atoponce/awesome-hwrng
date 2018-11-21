# Awesome Hardware Random Number Generators

[//]: # (Spaces, not tabs. Disable line-wrapping. Align columns.)
[//]: # (Use arbitrary-text links in general. Prefer HTTPS if available.)

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

This table is a list of hardware random number generators that was initially on
[Wikipedia], but has since been removed, as it did not meet certain guidelines.

[Wikipedia]: https://en.wikipedia.org/wiki/Wikipedia:Articles_for_deletion/Comparison_of_hardware_random_number_generators

Table sort is not supported in Github like it is in Wikipedia, but if you
install [Greasemonkey] and the [Github Sort Content] user script in your
browser, you will then be able to sort the table columns.

[Greasemonkey]: https://www.greasespot.net/
[Github Sort Content]: https://greasyfork.org/en/scripts/21373-github-sort-content

[//]: # (For citation links, use last 4 hex characters of the SHA-256 of the link.)
[//]: # (This allows links to be easily reused without keeping track of counters)
[//]: # (EG: $ printf 'https://www.gniibe.org/memo/development/gnuk/rng/neug.html' | sha256sum | cut -f 1 -d ' ' | tail -c 5)
[//]: # (Place at bottom of README)

## External HWRNGs
These are externally available HWRNGs that you can plug into your computer,
usually via USB, but PCIe, network, and even old-school DE-9 serial.

| Builder                 | Model                   | Interface  | Price         | Mbps          | Entropy                             | Hardware     | Software              |
| ----------------------- | ----------------------- | :--------: | :-----------: | :-----------: | ----------------------------------- | ------------ | --------------------- |
| Altus Metrum            | [ChaosKey 1.0]          | USB        | [$40][6ea7]   | [10][00dc]    | [Reverse biased p-n junction][00dc] | [Open][88f0] | [GPLv2][f4bd]         |
| Araneus                 | [Alea II]               | USB        | [€109][e0f5]  | [0.1][84f9]   | [Reverse biased p-n junction][84f9] | Closed       | Proprietary           |
| Bitbabbler              | [BitBabbler Black]      | USB        | [$49][d312]   | [0.65][7859]  | [Shot noise][22bb]                  | Closed       | [GPLv2][043f]         |
| Bitbabbler              | [BitBabbler White]      | USB        | [$199][d312]  | [2.5][deb1]   | [Shot noise][22bb]                  | Closed       | [GPLv2][043f]         |
| Comscire                | [PQ128MS]               | USB        | [$1845][6b64] | [128][6b64]   | [Shot noise][6b64]                  | Closed       | Proprietary           |
| Comscire                | [PQ32MS]                | USB        | [$1445][e967] | [32][e967]    | [Shot noise][e967]                  | Closed       | Proprietary           |
| Comscire                | [PQ32MU]                | USB        | [$1095][ecdb] | [32][ecdb]    | [Shot noise][ecdb]                  | Closed       | Proprietary           |
| Comscire                | [PQ4000KSI]             | USB        | [$765][f06c]  | [4][f06c]     | [Shot noise][f06c]                  | Closed       | Proprietary           |
| Comscire                | [PQ4000KS]              | USB        | [$795][c384]  | [4][c384]     | [Shot noise][c384]                  | Closed       | Proprietary           |
| Flying Stone Technology | [NeuG]                  | USB        | [$50][c826]   | [0.640][229d] | [ADC noise][229d]                   | [Open][ffd7] | [GPLv3][ffd7]         |
| Generic                 | [RTL-SDR] dongles       | USB        | [$22][269e]   | [2.8][086d]   | [Atmospheric noise][b331]           | Closed       | [GPLv3][b331]         |
| Generic                 | Any webcam              | USB        | [$7][a173]    | [0.96][7767]  | [Image noise][aa8c]                 | Closed       | [Public domain][f717] |
| IDQ                     | [Quantis USB]           | USB        | [€990][de84]  | [4][448b]     | [Beam splitter][3095]               | Closed       | Proprietary           |
| IDQ                     | [Quantis PCIe-4M]       | PCIe       | [€1299][de84] | [4][448b]     | [Beam splitter][3095]               | Closed       | Proprietary           |
| IDQ                     | [Quantis PCIe-16M]      | PCIe       | [€2990][de84] | [16][448b]    | [Beam splitter][3095]               | Closed       | Proprietary           |
| IDQ                     | [Quantis Appliance 4M]  | Network    | N/A           | [4][f083]     | [Beam splitter][3095]               | Closed       | Proprietary           |
| IDQ                     | [Quantis Appliance 16M] | Network    | N/A           | [16][f083]    | [Beam splitter][3095]               | Closed       | Proprietary           |
| IDQ                     | [Quantis AIS31]         | PCIe & USB | N/A           | [0.075][f988] | [Beam splitter][3095]               | Closed       | Proprietary           |
| Intel                   | [Ivy Bridge]            | CPU        | Varies        | [3000][9c29]  | [Johnson-Nyquist noise][9c29]       | Closed       | Mixed                 |
| Kidekin                 | [DigitalTRNG]           | USB        | N/A           | [2][5fa9]     | [Registerless LFSR][5fa9]           | Closed       | Proprietary           |
| Moonbase Otago          | [OneRNG]                | USB        | [$40][fe95]   | [0.35][7e61]  | [Avalanche noise][1115]             | [Open][17a3] | [GPLv3][17a3]         |
| Protego ST              | [SG100 Classic]         | Serial     | [€255][ded5]  | [0.115][ded5] | [Reverse biased zener diode][c6c8]  | Closed       | Proprietary           |
| Protego ST              | [SG100 EVO-USB]         | USB        | [€279][b49e]  | [0.115][b49e] | [Reverse biased zener diode][c6c8]  | Closed       | Proprietary           |
| Protego ST              | [SG100 EVO-USB CERT]    | USB        | [€530][edcd]  | [0.115][edcd] | [Reverse biased zener diode][c6c8]  | Closed       | Proprietary           |
| QuintessenceLabs        | [qStream]               | Network    | N/A           | [1000][d37a]  | [Tunnel diode][2215]                | Closed       | Proprietary           |
| Simtec Electronics      | [Entropy Key]           | USB        | [£36][7bd0]   | [0.032][a538] | [Reverse biased p-n junction][91fa] | Closed       | [MIT][e8cf]           |
| TectroLabs              | [SwiftRNG-LE]           | USB        | [$149][b31f]  | [20][b31f]    | [Reverse biased Zener diode][b31f]  | Closed       | Proprietary           |
| TectroLabs              | [SwiftRNG]              | USB        | [$249][b31f]  | [100][b31f]   | [Reverse biased Zener diode][b31f]  | Closed       | Proprietary           |
| TectroLabs              | [SwiftRNG-Pro]          | USB        | [$449][b31f]  | [200][b31f]   | [Reverse biased Zener diode][b31f]  | Closed       | Proprietary           |
| TRNG98                  | [TRNG9803]              | Serial     | [€49][633d]   | 0.072         |                                     | Closed       | Proprietary           |
| TRNG98                  | [TRNG9815]              | USB        | [€478][1499]  | 0.550         |                                     | Closed       | Proprietary           |
| ubld.it                 | [TrueRNG v2]            | USB        | [$50][f7cf]   | [0.35][f7cf]  | [Reverse-biased p-n junction][f7cf] | Closed       | Proprietary           |
| ubld.it                 | [TrueRNG v3]            | USB        | [$50][e123]   | [0.4][e123]   | [Reverse-biased p-n junction][e123] | Closed       | Proprietary           |
| ubld.it                 | [TrueRNGpro]            | USB        | [$100][40ff]  | [3.2][40ff]   |                                     | Closed       | Proprietary           |
| Vault12                 | [TrueEntropy]           | iOS        | Varies        | [0.3][36fe]   | [Image noise][af49]                 | Closed       | [MIT][36fe]           |
| WaywardGeek             | [Infinite Noise]        | USB        | [$35][4683]   | [0.3][3571]   | [Johnson-Nyquist noise][3571]       | [Open][3571] | [Public Domain][3571] |

## Embedded HWRNGs
These are generators that are on CPUs, either provided stand-alone, as in the
case for Intel and AMD, or as part of a SoC as in the case of Raspberry Pi. They
may also be components for breadboard, solder, or other engineering projects

| Builder                 | Model                   | Interface  | Price         | Mbps          | Entropy                             | Hardware     | Software              |
| ----------------------- | ----------------------- | :--------: | :-----------: | :-----------: | ----------------------------------- | ------------ | --------------------- |
| Generic                 | [STM32 Nucleo boards]   | USB        | $12   | 0.56  | Analog-to-digital converter noise | Closed | GPLv3 |
| TRNG98                  | TRNG9880 | USB | €620 | 0.55 | | Closed | Proprietary |

## Hardware Security Module HWRNGs
There are generators provided as part of HSMs, whether they are external USB
devices, part of a smart device, or shipped in hardware for server platforms

| Builder                 | Model                   | Interface  | Price         | Mbps          | Entropy                             | Hardware     | Software              |
| ----------------------- | ----------------------- | :--------: | :-----------: | :-----------: | ----------------------------------- | ------------ | --------------------- |

[//]: # (Reference links here- sorted by ID)
[Alea II]: https://www.araneus.fi/products/alea2/en/
[BitBabbler Black]: http://www.bitbabbler.org/what.html#BitBabbler-Black
[BitBabbler White]: http://www.bitbabbler.org/what.html#BitBabbler-White
[ChaosKey 1.0]: https://altusmetrum.org/ChaosKey/
[DigitalTRNG]: http://kidekin.nimp.co.uk/
[Entropy Key]: http://www.entropykey.co.uk/
[Infinite Noise]: https://www.tindie.com/products/WaywardGeek/infinite-noise-true-random-number-generator/
[Ivy Bridge]: https://en.wikipedia.org/wiki/Ivy_Bridge_(microarchitecture)
[NeuG]: https://www.gniibe.org/category/fst-01.html
[OneRNG]: http://onerng.info/
[PQ128MS]: https://comscire.com/product/pq128ms/
[PQ32MS]: https://comscire.com/product/pq32ms/
[PQ32MU]: https://comscire.com/product/pq32mu/
[PQ4000KSI]: https://comscire.com/product/pq4000ksi/
[PQ4000KS]: https://comscire.com/product/pq4000ks/
[qStream]: https://www.quintessencelabs.com/products/qstream-quantum-true-random-number-generator/
[Quantis USB]: https://www.idquantique.com/random-number-generation/products/quantis-random-number-generator/
[Quantis PCIe-4M]: https://www.idquantique.com/random-number-generation/products/quantis-random-number-generator/
[Quantis PCIe-16M]: https://www.idquantique.com/random-number-generation/products/quantis-random-number-generator/
[Quantis Appliance 4M]: https://www.idquantique.com/random-number-generation/products/quantis-rng-appliance/
[Quantis Appliance 16M]: https://www.idquantique.com/random-number-generation/products/quantis-rng-appliance/
[Quantis AIS31]: https://www.idquantique.com/random-number-generation/products/quantis-rng-appliance/
[RTL-SDR]: https://www.rtl-sdr.com/
[SG100 Classic]: https://www.protegost.com/product-page/sg100-classic
[SG100 EVO-USB]: https://www.protegost.com/product-page/sg100-evo
[SG100 EVO-USB CERT]: https://www.protegost.com/product-page/sg100-evo-cert
[SwiftRNG-LE]: https://tectrolabs.com/swiftrng-le/
[SwiftRNG]: https://tectrolabs.com/swiftrng-100/
[SwiftRNG-Pro]: https://tectrolabs.com/swiftrng-pro/
[TRNG9803]: http://www.trng98.se/serial_trng_9803.html
[TRNG9815]: http://www.trng98.se/usb_trng_9815.html
[TrueRNG v2]: http://ubld.it/products/truerng-hardware-random-number-generator/
[TrueRNG v3]: http://ubld.it/truerng_v3
[TrueRNGpro]: http://ubld.it/products/truerngpro

[//]: # (Citation links here- sorted by ID)
[00dc]: https://debconf16.debconf.org/talks/94/
[043f]: http://www.bitbabbler.org/what.html#download
[086d]: https://pthree.org/2015/06/16/hardware-rng-through-an-rtl-sdr-dongle/
[1115]: http://www.moonbaseotago.com/onerng/theory.html
[1499]: http://www.trng98.se/shop/product_info.php?products_id=34
[17a3]: http://www.moonbaseotago.com/onerng/#license
[2215]: https://www.quintessencelabs.com/press_release/quantum-tunneling-away-cyber-criminals/
[229d]: https://www.gniibe.org/memo/development/gnuk/rng/neug.html
[22bb]: http://www.bitbabbler.org/how.html
[269e]: https://www.amazon.com/dp/B00P2UOU72/
[3095]: https://marketing.idquantique.com/acton/attachment/11868/f-0227/1/-/-/-/-/Quantum%20RNG_White%20Paper.pdf
[3571]: https://github.com/waywardgeek/infnoise/
[36fe]: https://github.com/vault12/TrueEntropy
[40ff]: http://ubld.it/products/truerngpro
[448b]: https://www.idquantique.com/random-number-generation/products/quantis-random-number-generator/
[4683]: https://www.tindie.com/products/WaywardGeek/infinite-noise-true-random-number-generator/
[49ac]: http://www.trng98.se/trng98_encryption_documents/non-algorithmic%20encryption.pdf
[5fa9]: https://www.tindie.com/products/kidekin/digitaltrng/
[633d]: http://www.trng98.se/shop/product_info.php?products_id=33
[6b64]: https://comscire.com/product/pq128ms/
[6ea7]: https://shop.gag.com/random.html
[7bd0]: http://www.entropykey.co.uk/shop/
[7e61]: http://www.moonbaseotago.com/onerng/
[7767]: https://pthree.org/2017/12/22/the-entropy-of-a-digital-camera-ccd-cmos-sensor/
[7859]: http://www.bitbabbler.org/what.html#BitBabbler-Black
[84f9]: https://www.araneus.fi/products/alea2/en/
[88f0]: https://git.gag.com/?p=hw/chaoskey;a=blob_plain;f=License.pdf;hb=HEAD
[91fa]: http://www.entropykey.co.uk/tech/
[9c29]: https://software.intel.com/en-us/articles/intel-digital-random-number-generator-drng-software-implementation-guide
[a173]: https://www.amazon.com/dp/B0072I2240/
[a538]: https://pthree.org/2012/10/05/the-entropy-key/
[aa8c]: https://www.hindawi.com/journals/mpe/2013/285373/
[af49]: https://medium.com/vault12/how-to-get-true-randomness-from-your-apple-device-with-particle-physics-and-thermal-entropy-a9d47ca80c9b
[b31f]: https://tectrolabs.com/swiftrng/
[b331]: https://github.com/pwarren/rtl-entropy
[b49e]: https://www.protegost.com/product-page/sg100-evo
[c384]: https://comscire.com/product/pq4000ks/
[c6c8]: https://docs.wixstatic.com/ugd/a434f2_15a22f7e064040ceafe58391d6c6e23f.pdf
[c826]: https://shop.fsf.org/storage-devices/neug-usb-true-random-number-generator
[d312]: http://www.bitbabbler.org/buy.html
[d37a]: https://www.quintessencelabs.com/products/qstream-quantum-true-random-number-generator/
[de84]: https://www.idquantique.com/shop/online-shop/
[deb1]: http://www.bitbabbler.org/what.html#BitBabbler-White
[ded5]: https://www.protegost.com/product-page/sg100-classic
[e0f5]: https://www.araneus.fi/products/alea2/order/en/
[e123]: http://ubld.it/truerng_v3
[e8cf]: http://www.entropykey.co.uk/download/
[e967]: https://comscire.com/product/pq32ms/
[ecdb]: https://comscire.com/product/pq32mu/
[edcd]: https://www.protegost.com/product-page/sg100-evo-cert
[f06c]: https://comscire.com/product/pq4000ksi/
[f083]: https://www.idquantique.com/random-number-generation/products/quantis-rng-appliance/
[f4bd]: https://git.gag.com/?p=fw/altos;a=blob_plain;f=COPYING;hb=HEAD
[f717]: https://github.com/atoponce/scripts/blob/master/webcam_rng.py
[f7cf]: http://ubld.it/products/truerng-hardware-random-number-generator/
[f988]: https://www.idquantique.com/random-number-generation/products/quantis-ais-31/
[fe95]: https://moonbase.tictail.com/
[ffd7]: https://salsa.debian.org/gnuk-team/gnuk/neug
