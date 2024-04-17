# UEB-Testsuite
A student created testsuite for the [Übersetzterbau (Compilers)](https://tiss.tuwien.ac.at/course/courseDetails.xhtml?dswid=3349&dsrid=144&courseNr=185A48&semester=2024S) VU at [TU Wien](https://www.tuwien.at/en/) in 2024S.

[Previous year's test suite](https://github.com/RFJBraunstingl/UEB-Testsuite-2023S)

## Usage
1. `git clone https://github.com/AntiKippi/UEB-Testsuite-2024S ~/test`
2. The tests starting from the "scanner" example should be picked up automatically the the test scripts on the server

## Tips
With the following optional convenience function added to your `.bashrc` you can run the test suite by executing `runtest <exercise>` or simply `runtest` if you are in the directory you want to test:
```
function runtest() {
    target="$1"
    if [ -z "$target" ]; then
        target="$(basename "$PWD")"
    fi
    git -C ~/test pull && "/usr/ftp/pub/ubvl/test/${target}/test"
}
```

## Notes
- If you write your own tests, please share them by creating a pull request
- If you choose to do so please use the following naming convention to avoid conflicts: `{username}_{description}.{type}` (e.g. `AntiKippi_comments.0`)
