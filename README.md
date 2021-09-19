# ferrugem

![](https://github.com/leapofazzam123/ferrugem/raw/principal/logo.jpeg)

Aren't you _cansado_ from writing Rust programs in English? Do you like saying
"caralho" a lot? Would you like to try something different, in an exotic and
funny-sounding language? Would you want to bring some Portugese touch to your
programs?

**ferrugem** (Portugese for _Rust_) is here to save your day, as it allows you to
write Rust programs in Portuguese, using Portuguese keywords, Portugese function names,
Portuguese idioms.

You're from Brazil but don't feel at ease using only Portuguese words? Don't worry!
Portuguese Rust is fully compatible with English-Rust, so you can mix both at your
convenience.

Here's an example of what can be achieved with Ferrugem:

### trait and impl (aka peculiaridade e implementação)

```rust
rouille::rouille! {
    utilisons std::collections::Dictionnaire comme Dico;

    convention CléValeur {
        fonction écrire(&soi, clé: Chaine, valeur: Chaine);
        fonction lire(&soi, clé: Chaine) -> PeutÊtre<&Chaine>;
    }

    statique mutable DICTIONNAIRE: PeutÊtre<Dico<Chaine, Chaine>> = Rien;

    structure Concrète;

    réalisation CléValeur pour Concrète {
        fonction écrire(&soi, clé: Chaine, valeur: Chaine) {
            soit dico = dangereux {
                DICTIONNAIRE.prendre_ou_insérer_avec(Défaut::défaut)
            };
            dico.insérer(clé, valeur);
        }
        fonction lire(&soi, clé: Chaine) -> Résultat<PeutÊtre<&Chaine>, Chaine> {
            si soit Quelque(dico) = dangereux { DICTIONNAIRE.en_réf() } {
                Bien(dico.lire(&clé))
            } sinon {
                Arf("fetchez le dico".vers())
            }
        }
    }
}
```

### Support for regional languages

```rust
#[légal(code_inaccessible)]
fonction secondaire() {
    merde!("oh non"); // for the true French experience
    calisse!("tabarnak"); // for friends speaking fr-ca
    oups!("fetchez la vache"); // in SFW contexts
}
```

### Other examples

See the [examples](./examples/src/main.rs) to get a rough sense of the whole
syntax. Voilà, that's it.

## Contribuições

First of all, _muito obrigado_ for considering participating to this joke, the
Brazil government will thank you later! Feel free to throw in a few identifiers
here and there, and open a pull-request against the `principal` (Portuguese for
`main`) branch.

Please don't introduce swear words, though: we will not excuse your Portuguese.

## mas por que você faria isso?

- because brazil memes

## Other languages

- Dutch: [roest](https://github.com/jeroenhd/roest)
- German: [rost](https://github.com/michidk/rost)
- Polish: [rdza](https://github.com/phaux/rdza)
- Italian: [ruggine](https://github.com/DamianX/ruggine)
- Russian: [ржавчина](https://github.com/FluxIndustries/rzhavchina)
- Esperanto: [rustteksto](https://github.com/dscottboggs/rustteksto)
- Hindi: [zung](https://github.com/rishit-khandelwal/zung)
- Hungarian: [rozsda](https://github.com/jozsefsallai/rozsda)
- Chinese: [xiu (锈)](https://github.com/lucifer1004/xiu)
- Spanish: [oxido](https://github.com/fdschonborn/oxido)
- Korean: [Nok (녹)](https://github.com/Alfex4936/nok)
- Finnish: [ruoste](https://github.com/vkoskiv/ruoste)
- Arabic: [sada](https://github.com/LAYGATOR/sada)

## un grand merci

- [@bnjbvr](https://github.com/bnjbvr/rouille) for the original version (rouille)

## a licença

[WTFPL](http://www.wtfpl.net/).
