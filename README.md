# Google Fonts Lint (Java)

This Java lint tools will check a directory is ready for inclusion in [github.com/google/fonts](http://github.com/google/fonts)

This is not an official Google project, and Google provides no support for it.

To build the `lint.jar` executable, run:

```sh
ant lint-jar;
```

To run the lint tool on the entire Google Fonts collection, run:

```sh
for metadata in $(find /path/to/google/fonts/{ofl,ufl,apache} -name METADATA.json); do
  java -jar /path/to/lint/dist/lint.jar "$(dirname $metadata)";
done
```

