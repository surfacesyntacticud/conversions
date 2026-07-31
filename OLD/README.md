# Obsolete material

This folder contains obsolete material that is not maintained and is not expected to work out of the box.

It is kept here for reference purposes only.

---

## Automatic tests
You can run automatic tests defined in `./test2/tests_description.json` to see if the rules are being applied correctly.
You need to add a folder that has the same name of the grs file inside `test2/data/` with both a `source.conllu` and an `expected conllu`.

### test description
Add an entry for your grs rule inside `./test2/tests_description.json` with the following entries :
```json
[
    {
        "TEST_FOLDER_NAME": "zh_mSUD_to_SUD",
        "GRS_FILE": "zh_mSUD_to_SUD.grs",
        "STRAT_NAME": "zh_mSUD_to_SUD_main",
        "CONFIG_TYPE": "sud"
    }
]
```

### Tests command
Using docker, run the following commands

```bash
docker build -t grs_test . 
docker run grs_test
```

