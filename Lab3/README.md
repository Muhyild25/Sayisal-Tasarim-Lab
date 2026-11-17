# Lab 3: Decoder ve Multiplexer ile Kombinasyonel Tasarım

Kombinasyonel devreler MSI entegreleriyle (74151 multiplexer, 74154 decoder) gerçeklendi. Uzun doğruluk tablolarının temel kapılara göre çok daha az donanımla çözülebildiği gözlemlendi.

| Dosya | Açıklama |
|-------|----------|
| `Odd-Parity-Generator.circ` | 74151 ile 4 bitlik **tek eşlik** (odd parity) üreteci: kodda 1'lerin sayısı çift ise P=1 |
| `Parity-Generator-Mux.circ` | Aynı üreteç, A ve B seçme hattı olarak kullanılarak tasarlandı. Veri girişleri C XNOR D ve C XOR D |
| `Even-Odd-Sum-74154-NAND.circ` | İki 2-bitlik sayının (A, B) toplamı tek ise Z1, çift ise Z2 çıkışı. Bir adet 74154 decoder ve yalnızca NAND kapıları (7430) kullanıldı |
| `Even-Odd-Sum-3to8-Decoders.circ` | Aynı fonksiyon iki adet 3-to-8 decoder ile. A1, iki decoder arasında enable sinyaliyle seçim yapar |

**Not:** 74154 çıkışları aktif-düşük olduğu için, ilgili minterm çıkışları NAND kapısına bağlanarak ek NOT veya OR kapısına gerek kalmadan doğru lojik seviye elde edildi.

**Kütüphane:** `74TTLs_1.03`
