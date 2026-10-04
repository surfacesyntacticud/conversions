
# The UD/SUD converter tool

This repository contains a set of Graph Rewriting rules which can be used with the [Grew software](http://grew.fr) for conversion from [UD](http://universaldependencies.org/) to [SUD](https://surfacesyntacticud.org/) and the other way.

Examples of converted data are available [here](https://surfacesyntacticud.org/data).

## HOWTO use the conversion system

You first have to install the most recent version of the Grew software (see [instructions](https://grew.fr/usage/install/) page).

### Universal conversion from UD to SUD

```
grew transform -grs grs/UD_to_SUD.grs -config sud -i input_UD_file.conllu -o output_SUD_file.conllu
```

### Universal conversion from SUD to UD

```
grew transform -grs grs/SUD_to_UD.grs -config sud -i input_SUD_file.conllu -o output_UD_file.conllu
```

### Language specific conversions
For some languages, there are dedicated conversion systems.
Corresponding files are prefixed by the language code, for instance, `zh_SUD_to_UD.grs` is a conversion from SUD to UD adapted to Chinese annotations;
the strategy to used is names like the file with suffix `_main`(`zh_SUD_to_UD_main` in the previous example).
Consult the `grs` folder to see which languages have specific conversions systems.

