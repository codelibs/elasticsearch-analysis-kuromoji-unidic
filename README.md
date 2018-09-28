Elasticsearch Analysis Kuromoji Unidic
=======================

## Overview

Elasticsearch Analysis Kuromoji Plugin provides Tokenizer/CharFilter/TokenFilter for Kuromoji with Unidic.

## Version

[Versions in Maven Repository](http://central.maven.org/maven2/org/codelibs/elasticsearch-analysis-kuromoji-unidic/)

### Issues/Questions

Please file an [issue](https://github.com/codelibs/elasticsearch-analysis-kuromoji-unidic/issues "issue").
(Japanese forum is [here](https://github.com/codelibs/codelibs-ja-forum "here").)

## Installation

### For 5.x - 6.x

    $ $ES_HOME/bin/elasticsearch-plugin install org.codelibs:elasticsearch-analysis-kuromoji-unidic:5.6.1

### For 2.x

    $ $ES_HOME/bin/plugin install org.codelibs/elasticsearch-analysis-kuromoji-unidic/2.4.1

## References

### Analyzer, Tokenizer, TokenFilter, CharFilter

The plugin includes these analyzer and tokenizer, tokenfilter.

| name                                     | type        |
|:-----------------------------------------|:-----------:|
| kuromoji\_unidic\_iteration\_mark       | charfilter  |
| kuromoji\_unidic                        | analyzer    |
| kuromoji\_unidic\_tokenizer             | tokenizer   |
| kuromoji\_unidic\_baseform              | tokenfilter |
| kuromoji\_unidic\_part\_of\_speech      | tokenfilter |
| kuromoji\_unidic\_readingform           | tokenfilter |
| kuromoji\_unidic\_stemmer               | tokenfilter |

### Usage

See [Elasticsearch Kuromoji](https://github.com/elastic/elasticsearch-analysis-kuromoji "elasticsearch-analysis-kuromoji").

### Update Kuromoji Jar File

If you want to replace with the latest Lucene Unidic jar file, download it from http://maven.codelibs.org/org/codelibs/lucene-analyzers-kuromoji-unidic/ and then replace old file in $ES_HOME/plugins/analysis-kuromoji-unidic.

### What is UniDic

See [mecab-unidic](https://ja.osdn.net/projects/unidic/).

## Use Lucene Kuromoji for UniDic

If you want to use Lucene Kuromoji for Unidic in your application other than elasticsearch, you can use lucene-analyzers-kuromoji-unidic jar file, not this plugin.
To use the jar file, put the following settings into your pom.xml.

    ...
    <repositories>
        <repository>
            <id>codelibs.org</id>
            <name>CodeLibs Repository</name>
            <url>http://maven.codelibs.org/</url>
        </repository>
    </repositories>
    ...
    <dependencies>
        <dependency>
            <groupId>org.codelibs</groupId>
            <artifactId>lucene-analyzers-kuromoji-unidic</artifactId>
            <version>7.4.0-2_1_2</version>
        </dependency>
    ...

See [CodeLibs Maven Repository](http://maven.codelibs.org/org/codelibs/lucene-analyzers-kuromoji-unidic/).

