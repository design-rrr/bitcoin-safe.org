---
title: "Seed COLDCARD insegura"
date: "2026-08-02"
draft: false
description: "Guia mínima per traslladar fons des d'una seed generada en un dispositiu Coinkite."
---

[Coinkite ha revelat una feblesa en la generació de seeds del firmware COLDCARD afectat](https://blog.coinkite.com/coldcard-mk3-seed-generation-warning/). Consulta també [l'anàlisi tècnica de Block sobre el fallback predictible de l'RNG i el reseed de 32 bits](https://engineering.block.xyz/blog/predictable-rng-fallback-and-32-bit-reseed-in-coldcard-firmware). Actualitzar el firmware no repara una seed existent.

**Si has creat una seed amb qualsevol producte Coinkite, migra AVIAT!**

## Llista de migració

1. En un **dispositiu de signatura que no sigui COLDCARD** ([consulta els dispositius compatibles]({{< ref "library/supported-hardware-signers" >}})), crea un moneder completament nou amb l'assistent de configuració de Bitcoin-Safe: tria un [moneder de signatura única]({{< ref "library/setup-singlesig-wallet" >}}) o un [moneder multifirma]({{< ref "library/setup-multisig-wallet" >}}). No reutilitzis la seed antiga.
   - Si no tens disponible cap signador de maquinari que no sigui COLDCARD, [MetroVault]({{< ref "library/supported-hardware-signers/metrovault" >}}) és una opció en un dispositiu Android dedicat, restablert de fàbrica, mantingut fora de línia i utilitzat només per signar.
   - Completa la prova de recepció i enviament de l'assistent per assegurar-te que el moneder nou està ben configurat: verifica'n la còpia de seguretat i una adreça de recepció al signador nou, rep una petita quantitat de prova i fes correctament un autoenviament a una altra adreça verificada del moneder nou.
2. Signa la transacció de migració, però **no la difonguis de la manera habitual**. Copia la transacció en brut signada i envia-la directament mitjançant [MARA Slipstream](https://slipstream.mara.com/) per reduir el temps durant el qual les claus públiques del moneder antic queden exposades a la mempool pública.
3. Conserva el COLDCARD antic fins que el saldo complet hagi arribat i s'hagi confirmat al moneder nou; després, actualitza'l al firmware més recent.

Si ajudes algú a migrar, no li demanis mai que comparteixi, fotografiï o escrigui les paraules de la seed. La seed ha de romandre privada i introduir-se només al dispositiu de signatura.
