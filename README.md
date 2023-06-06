# shortboost
This repository offers a way to translate single Unicode characters into multiple characters in domain names or TLDs. The primary benefit of this lies in condensing domain payloads, which is extremely useful for situations where character counts are limited, such as in [XSS attacks](https://github.com/ssl/ezXSS).

Instead of purchasing very short domains, this allows you to create domain names that are as short as three characters, including the dot. This is shorter than conventional domain names, making your payloads significantly more compact.

These translations are **not** using punycode, which typically translates into the format `xn--`. Rather, they translate into the represented English characters directly.

For reference, the shortest conventional domain is four characters, in the format `x.xx`. By using these characters, you can reduce a 8 character domain to just three characters. For instance, `ⅷ.℡` translates into `viii.tel`.

If you find any character missing or have any improvements to suggest, please feel free to open an issue or make a pull request.


| Character | Unicode | Representation | Is buyable TLD |
|-----------|---------|----------------|--------|
| ĳ         | U+0133  | ij             | ❌       |
| ㍴         | U+3374  | bar            |  ✅ $3    |
| ㍵         | U+3375  | ov             |  ❌      |
| ㎁         | U+3382  | na             |  ✅ $5000     |
| ㎃         | U+3384  | ma             |   ➖ $20     |
| ㎄         | U+3385  | ka             |    ❌    |
| ㎅         | U+3386  | kb             |   ❌     |
| ㎆         | U+3387  | mb             |   ❌     |
| ㎇         | U+3388  | gb             |    ❌    |
| ㎈         | U+3389  | cal            |   ❌     |
| ㎉         | U+338A  | kcal           |  ❌      |
| ㎊         | U+338B  | pf             |  ➖ $200      |
| ㎋         | U+338C  | nf             |  ✅ $110     |
| ㎎         | U+338F  | mg             |    ➖ $100    |
| ㎏         | U+3390  | kg             |    ✅ $70   |
| ㎐         | U+3391  | hz             |   ❌     |
| ㎑         | U+3392  | khz            |   ❌     |
| ㎒         | U+3393  | mhz            |   ❌     |
| ㎓         | U+3394  | ghz            |  ❌      |
| ㎔         | U+3395  | thz            |   ❌     |
| ㎖         | U+3397  | ml             |    ✅ $0   |
| ㎗         | U+3398  | dl             |  ❌      |
| ㎘         | U+3399  | kl             |  ❌      |
| ㎙         | U+339A  | fm             |   ✅ $70    |
| ㎚         | U+339B  | nm             |   ❌     |
| ㎜         | U+339D  | mm             |   ❌     |
| ㎝         | U+339E  | cm             |   ✅ $70    |
| ㎞, ㏎         | U+339F,CF  | km             |   ✅ $300    |
| ㎟         | U+33A0  | mm2            |  ❌      |
| ㎠         | U+33A1  | cm2            |  ❌      |
| ㎡         | U+33A2  | m2             |  ❌      |
| ㎢         | U+33A3  | km2            |  ❌      |
| ㎣         | U+33A4  | mm3            |  ❌      |
| ㎤         | U+33A5  | cm3            |   ❌     |
| ㎥         | U+33A6  | m3             |   ❌     |
| ㎦         | U+33A7  | km3            |   ❌     |
| ㎩, ㎀         | U+33AA,81  | pa             |   ✅ $150     |
| ㎪         | U+33AB  | kpa            |   ❌     |
| ㎫         | U+33AC  | mpa            |   ❌     |
| ㎬         | U+33AD  | gpa            |   ❌     |
| ㎭         | U+33AE  | rad            |   ❌     |
| ㎰         | U+33B1  | ps             |   ✅ $50     |
| ㎱         | U+33B2  | ns             |  ❌      |
| ㎳         | U+33B4  | ms             |   ✅     |
| ㎴         | U+33B5  | pv             |   ❌     |
| ㎵         | U+33B6  | nv             |   ❌     |
| ㎷,㎹         | U+33B8,A  | mv             |  ✅ $250      |
| ㎸         | U+33B9  | kv             |    ❌    |
| ㎺         | U+33BB  | pw             |   ✅ $1     |
| ㎻         | U+33BC  | nw             |  ❌      |
| ㎽, ㎿         | U+33BE,C0  | mw             |   ✅ $70     |
| ㎾         | U+33BF  | kw             |   ❌     |
| ㏂         | U+33C3  | am             |   ✅ $25    |
| ㏃         | U+33C4  | bq             |  ❌      |
| ㏄         | U+33C5  | cc             |   ✅ $3    |
| ㏅         | U+33C6  | cd             |   ✅ $50     |
| ㏇         | U+33C8  | co             |  ✅ $3      |
| ㏈         | U+33C9  | db             |   ❌     |
| ㏉         | U+33CA  | gy             |   ✅ $30     |
| ㏊         | U+33CB  | ha             |  ❌      |
| ㏋         | U+33CC  | hp             |    ❌    |
| ㏌         | U+33CD  | in             |   ✅ $5     |
| ㏍         | U+33CE  | kk             |   ❌     |
| ㏏         | U+33D0  | kt             |  ❌      |
| ㏐         | U+33D1  | lm             |  ❌      |
| ㏑         | U+33D2  | ln             |   ❌     |
| ㏒         | U+33D3  | log            |   ❌     |
| ㏓         | U+33D4  | lx             |   ❌     |
| ㏔         | U+33D5  | mb             |    ❌    |
| ㏕         | U+33D6  | mil            |   ❌     |
| ㏖         | U+33D7  | mol            |   ❌     |
| ㏗         | U+33D8  | ph             |   ✅ $50     |
| ㏘         | U+33D9  | pm             |  ➖ $5     |
| ㏙         | U+33DA  | ppm            |  ❌      |
| ㏚         | U+33DB  | pr             |  ✅ $600      |
| ㏛         | U+33DC  | sr             |   ✅ $15     |
| ㏜         | U+33DD  | sv             |  ➖ $100      |
| ㏝         | U+33DE  | wb             |   ❌     |
| №         | U+2116  | no             |  ➖ $10      |
| ™         | U+2122  | tm             | ✅ $100       |
| ℡         | U+2121  | tel            | ✅ $10       |
| ₨         | U+20A8  | rs             |  ✅ $25      |
| ℠         | U+2120  | sm             |  ➖ $150     |
| ㏿         | U+33FF  | gal            |  ✅ $50      |
| ﬀ         | U+FB00  | ff             |   ❌     |
| ﬁ         | U+FB01  | fi             |  ➖ $10      |
| ﬂ         | U+FB02  | fl             |    ❌    |
| ﬃ         | U+FB03  | ffi            |  ❌      |
| ﬄ         | U+FB04  | ffl            |   ❌     |
| ﬅ, ﬆ         | U+FB05,6  | st             |  ✅ $15      |
| ㍷         | U+3377  | dm             |  ✅ $130     |
| ㍸         | U+3378  | dm2            | ❌       |
| ㍹         | U+3379  | dm3            | ❌       |
| ㍺         | U+337A  | iu             |  ❌      |
| ㍶         | U+3376  | pc             |   ❌     |
| ㋌         | U+32CC  | hg             |  ❌      |
| ㋍         | U+32CD  | erg            |   ❌     |
| ㋎         | U+32CE  | ev             |   ❌     |
| ㋏         | U+32CF  | ltd            |  ✅ $1      |
| ㍱         | U+3371  | hpa            |  ❌      |
| ㍲         | U+3372  | da             |   ❌     |
| ㉐         | U+3250  | pte            |   ❌     |
| ⅸ         | U+2178  | ix             |    ❌    |
| ⅱ         | U+2171  | ii             |     ❌   |
| ⅲ         | U+2172  | iii            |    ❌    |
| ⅳ         | U+2173  | iv             |   ❌     |
| Ⅺ         | U+216A  | xi             |   ❌     |
| Ⅻ         | U+216B  | xii            |  ❌      |
| Ⅵ         | U+2165  | vi             | ➖ $300       |
| Ⅶ         | U+2166  | vii            |   ❌     |
| Ⅷ         | U+2167  | viii           |   ❌     |
| Ǌ, ǋ, ǌ   | U+01CA,B,C  | nj             |    ❌    |
| Ǳ, ǲ, ǳ   | U+01F1,2,3  | dz             |   ➖ $35     |
| Ǉ, ǈ      | U+01C7,8  | lj             |  ❌      |
| ⑩         | U+2469  | 10             | ❌       |
| ⑪         | U+246A  | 11             | ❌       |
| ⑫         | U+246B  | 12             | ❌       |
| ⑬         | U+246C  | 13             |  ❌      |
| ⑭         | U+246D  | 14             | ❌       |
| ⑮         | U+246E  | 15             | ❌       |
| ⑯         | U+246F  | 16             |  ❌      |
| ⑰         | U+2470  | 17             | ❌       |
| ⑱         | U+2471  | 18             | ❌       |
| ⑲         | U+2472  | 19             |  ❌      |
| ⑳         | U+2473  | 20             |  ❌      |
| ㉑         | U+3251  | 21             |  ❌      |
| ㉒         | U+3252  | 22             |  ❌      |
| ㉓         | U+3253  | 23             |  ❌      |
| ㉔         | U+3254  | 24             |  ❌      |
| ㉕         | U+3255  | 25             |   ❌     |
| ㉖         | U+3256  | 26             |   ❌     |
| ㉗         | U+3257  | 27             |  ❌      |
| ㉘         | U+3258  | 28             |   ❌     |
| ㉙         | U+3259  | 29             |   ❌     |
| ㉚         | U+325A  | 30             |   ❌     |
| ㉛         | U+325B  | 31             |   ❌     |
| ㉜         | U+325C  | 32             |   ❌     |
| ㉝         | U+325D  | 33             |   ❌     |
| ㉞         | U+325E  | 34             |   ❌     |
| ㉟         | U+325F  | 35             |   ❌     |
| ㊱         | U+32B1  | 36             |   ❌     |
| ㊲         | U+32B2  | 37             |   ❌     |
| ㊳         | U+32B3  | 38             |   ❌     |
| ㊴         | U+32B4  | 39             |  ❌      |
| ㊵         | U+32B5  | 40             |  ❌      |
| ㊶         | U+32B6  | 41             |  ❌      |
| ㊷         | U+32B7  | 42             |  ❌      |
| ㊸         | U+32B8  | 43             |  ❌      |
| ㊹         | U+32B9  | 44             |   ❌     |
| ㊺         | U+32BA  | 45             |   ❌     |
| ㊻         | U+32BB  | 46             |   ❌     |
| ㊼         | U+32BC  | 47             |   ❌     |
| ㊽         | U+32BD  | 48             |   ❌     |
| ㊾         | U+32BE  | 49             |   ❌     |
| ㊿         | U+32BF  | 50             |    ❌    |

- ✅ = Buyable
- ➖ = Buyable with restrictions
- ❌ = Cant buy for TLD, only usable in domain name
