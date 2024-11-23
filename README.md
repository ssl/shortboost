# shortboost
This repository offers a way to translate single Unicode characters into multiple characters in domain names or TLDs. The primary benefit of this lies in condensing domain payloads, which is extremely useful for situations where character counts are limited, such as in [XSS attacks](https://github.com/ssl/ezXSS).

Instead of purchasing very short domains, this allows you to create domain names that are as short as 3 characters, including the dot. This is shorter than conventional domain names, making your payloads significantly more compact.

These translations are **not** using punycode, which typically translates into the format `xn--`. Rather, they translate into the represented English characters directly.

For reference, the shortest conventional domain is 4 characters, in the format `x.xx`. By using these characters, you can reduce a 8 character domain to just 3 characters. For instance, `ⅷ.℡` translates into `viii.tel`.

If you find any character missing or have any improvements to suggest, please feel free to open an issue or make a pull request.


| Character | Unicode | Representation | Is buyable TLD |
|-----------|---------|----------------|--------|
 | ĳ | U+0133 | ij | ❌ | 
 | ㍴ | U+3374 | bar | ✅ $3 | 
 | ㍵ | U+3375 | ov | ❌ | 
 | ㎁ | U+3381 | na | ✅ $4500 | 
 | ㎃ | U+3383 | ma | ➖ $20 | 
 | ㎄ | U+3384 | ka | ❌ | 
 | ㎅ | U+3385 | kb | ❌ | 
 | ㎆ | U+3386 | mb | ❌ | 
 | ㎇ | U+3387 | gb | ❌ | 
 | ㎈ | U+3388 | cal | ❌ | 
 | ㎉ | U+3389 | kcal | ❌ | 
 | ㎊ | U+338A | pf | ➖ $200 | 
 | ㎋ | U+338B | nf | ✅ $110 | 
 | ㎎ | U+338E | mg | ➖ $100 | 
 | ㎏ | U+338F | kg | ✅ $65 | 
 | ㎐ | U+3390 | hz | ❌ | 
 | ㎑ | U+3391 | khz | ❌ | 
 | ㎒ | U+3392 | mhz | ❌ | 
 | ㎓ | U+3393 | ghz | ❌ | 
 | ㎔ | U+3394 | thz | ❌ | 
 | ㎖ | U+3396 | ml | ✅ $0 | 
 | ㎗ | U+3397 | dl | ❌ | 
 | ㎘ | U+3398 | kl | ❌ | 
 | ㎙ | U+3399 | fm | ✅ $70 | 
 | ㎚ | U+339A | nm | ❌ | 
 | ㎜ | U+339C | mm | ❌ | 
 | ㎝ | U+339D | cm | ✅ $70 | 
 | ㎞, ㏎ | U+339E, U+33CE | km | ✅ $300 | 
 | ㎟ | U+339F | mm2 | ❌ | 
 | ㎠ | U+33A0 | cm2 | ❌ | 
 | ㎡ | U+33A1 | m2 | ❌ | 
 | ㎢ | U+33A2 | km2 | ❌ | 
 | ㎣ | U+33A3 | mm3 | ❌ | 
 | ㎤ | U+33A4 | cm3 | ❌ | 
 | ㎥ | U+33A5 | m3 | ❌ | 
 | ㎦ | U+33A6 | km3 | ❌ | 
 | ㎩, ㎀ | U+33A9, U+3380 | pa | ✅ $150 | 
 | ㎪ | U+33AA | kpa | ❌ | 
 | ㎫ | U+33AB | mpa | ❌ | 
 | ㎬ | U+33AC | gpa | ❌ | 
 | ㎭ | U+33AD | rad | ❌ | 
 | ㎰ | U+33B0 | ps | ✅ $50 | 
 | ㎱ | U+33B1 | ns | ❌ | 
 | ㎳ | U+33B3 | ms | ✅ $30 | 
 | ㎴ | U+33B4 | pv | ❌ | 
 | ㎵ | U+33B5 | nv | ❌ | 
 | ㎷,㎹ | U+33B7, U+33B9 | mv | ✅ $250 | 
 | ㎸ | U+33B8 | kv | ❌ | 
 | ㎺ | U+33BA | pw | ✅ $1 | 
 | ㎻ | U+33BB | nw | ❌ | 
 | ㎽, ㎿ | U+33BD, U+33BF | mw | ✅ $70 | 
 | ㎾ | U+33BE | kw | ❌ | 
 | ㏃ | U+33C3 | bq | ❌ | 
 | ㏄ | U+33C4 | cc | ✅ $3 | 
 | ㏅ | U+33C5 | cd | ✅ $50 | 
 | ㏈ | U+33C8 | db | ❌ | 
 | ㏉ | U+33C9 | gy | ✅ $30 | 
 | ㏊ | U+33CA | ha | ❌ | 
 | ㏋ | U+33CB | hp | ❌ | 
 | ㏌ | U+33CC | in | ✅ $5 | 
 | ㏍ | U+33CD | kk | ❌ | 
 | ㏏ | U+33CF | kt | ❌ | 
 | ㏐ | U+33D0 | lm | ❌ | 
 | ㏑ | U+33D1 | ln | ❌ | 
 | ㏒ | U+33D2 | log | ❌ | 
 | ㏓ | U+33D3 | lx | ❌ | 
 | ㏔ | U+33D4 | mb | ❌ | 
 | ㏕ | U+33D5 | mil | ❌ | 
 | ㏖ | U+33D6 | mol | ❌ | 
 | ㏗ | U+33D7 | ph | ✅ $50 | 
 | ㏘ | U+33D8 | pm | ➖ $5 | 
 | ㏙ | U+33D9 | ppm | ❌ | 
 | ㏚ | U+33DA | pr | ✅ $600 | 
 | ㏛ | U+33DB | sr | ✅ $15 | 
 | ㏜ | U+33DC | sv | ➖ $100 | 
 | ㏝ | U+33DD | wb | ❌ | 
 | № | U+2116 | no | ➖ $10 | 
 | ™ | U+2122 | tm | ✅ $100 | 
 | ℡ | U+2121 | tel | ✅ $10 | 
 | ₨ | U+20A8 | rs | ✅ $25 | 
 | ℠ | U+2120 | sm | ➖ $150 | 
 | ㏿ | U+33FF | gal | ✅ $50 | 
 | ﬀ | U+FB00 | ff | ❌ | 
 | ﬁ | U+FB01 | fi | ➖ $10 | 
 | ﬂ | U+FB02 | fl | ❌ | 
 | ﬃ | U+FB03 | ffi | ❌ | 
 | ﬄ | U+FB04 | ffl | ❌ | 
 | ﬅ, ﬆ | U+FB05, U+FB06 | st | ✅ $15 | 
 | ㍷ | U+3377 | dm | ✅ $130 | 
 | ㍸ | U+3378 | dm2 | ❌ | 
 | ㍹ | U+3379 | dm3 | ❌ | 
 | ㍺ | U+337A | iu | ❌ | 
 | ㍶ | U+3376 | pc | ❌ | 
 | ㋌ | U+32CC | hg | ❌ | 
 | ㋍ | U+32CD | erg | ❌ | 
 | ㋎ | U+32CE | ev | ❌ | 
 | ㋏ | U+32CF | ltd | ✅ $1 | 
 | ㍱ | U+3371 | hpa | ❌ | 
 | ㍲ | U+3372 | da | ❌ | 
 | ㉐ | U+3250 | pte | ❌ | 
 | ⅸ | U+2178 | ix | ❌ | 
 | ⅱ | U+2171 | ii | ❌ | 
 | ⅲ | U+2172 | iii | ❌ | 
 | ⅳ | U+2173 | iv | ❌ | 
 | Ⅺ, ⅺ | U+216A, U+217A | xi | ❌ | 
 | Ⅻ, ⅻ | U+216B, U+217B | xii | ❌ | 
 | Ⅵ, ⅵ | U+2165, U+2175 | vi | ➖ $300 | 
 | Ⅶ, ⅶ | U+2166, U+2176 | vii | ❌ | 
 | Ⅷ, ⅷ | U+2167, U+2177 | viii | ❌ | 
 | Ǌ, ǋ, ǌ | U+01CA, U+01CB, U+01CC | nj | ❌ | 
 | Ǳ, ǲ, ǳ | U+01F1, U+01F2, U+01F3 | dz | ➖ $35 | 
 | Ǉ, ǈ | U+01C7, U+01C8 | lj | ❌ | 
 | ⑩ | U+2469 | 10 | ❌ | 
 | ⑪ | U+246A | 11 | ❌ | 
 | ⑫ | U+246B | 12 | ❌ | 
 | ⑬ | U+246C | 13 | ❌ | 
 | ⑭ | U+246D | 14 | ❌ | 
 | ⑮ | U+246E | 15 | ❌ | 
 | ⑯ | U+246F | 16 | ❌ | 
 | ⑰ | U+2470 | 17 | ❌ | 
 | ⑱ | U+2471 | 18 | ❌ | 
 | ⑲ | U+2472 | 19 | ❌ | 
 | ⑳ | U+2473 | 20 | ❌ | 
 | ㉑ | U+3251 | 21 | ❌ | 
 | ㉒ | U+3252 | 22 | ❌ | 
 | ㉓ | U+3253 | 23 | ❌ | 
 | ㉔ | U+3254 | 24 | ❌ | 
 | ㉕ | U+3255 | 25 | ❌ | 
 | ㉖ | U+3256 | 26 | ❌ | 
 | ㉗ | U+3257 | 27 | ❌ | 
 | ㉘ | U+3258 | 28 | ❌ | 
 | ㉙ | U+3259 | 29 | ❌ | 
 | ㉚ | U+325A | 30 | ❌ | 
 | ㉛ | U+325B | 31 | ❌ | 
 | ㉜ | U+325C | 32 | ❌ | 
 | ㉝ | U+325D | 33 | ❌ | 
 | ㉞ | U+325E | 34 | ❌ | 
 | ㉟ | U+325F | 35 | ❌ | 
 | ㊱ | U+32B1 | 36 | ❌ | 
 | ㊲ | U+32B2 | 37 | ❌ | 
 | ㊳ | U+32B3 | 38 | ❌ | 
 | ㊴ | U+32B4 | 39 | ❌ | 
 | ㊵ | U+32B5 | 40 | ❌ | 
 | ㊶ | U+32B6 | 41 | ❌ | 
 | ㊷ | U+32B7 | 42 | ❌ | 
 | ㊸ | U+32B8 | 43 | ❌ | 
 | ㊹ | U+32B9 | 44 | ❌ | 
 | ㊺ | U+32BA | 45 | ❌ | 
 | ㊻ | U+32BB | 46 | ❌ | 
 | ㊼ | U+32BC | 47 | ❌ | 
 | ㊽ | U+32BD | 48 | ❌ | 
 | ㊾ | U+32BE | 49 | ❌ | 
 | ㊿ | U+32BF | 50 | ❌ | 


- ✅ = Buyable
- ➖ = Buyable with restrictions
- ❌ = Cant buy for TLD, only usable in domain name

Is buyable TLD price sources: [tld-list.com](https://tld-list.com/), [domcomp.com](https://domcomp.com/)
