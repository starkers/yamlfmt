# yamlfmt

[![Build Status](https://travis-ci.com/wangkuiyi/yamlfmt.svg?branch=master)](https://travis-ci.com/wangkuiyi/yamlfmt)

I tried various beautifier of YAML files, but none of them satisfies me.

- https://pypi.org/project/yamlfmt cannot handle a file with multiple YAML objects separated by `---`.
- https://github.com/devopyio/yamlfmt cannot handle multiple files.
- https://github.com/miekg/yamlfmt/blob/master/fmt.go cannot replace (inline edit) the input files.

So, I decided to write this one based on https://github.com/miekg/yamlfmt/blob/master/fmt.go.

## Usage

- To beautify one or more files and write to stdout:

   ```bash
   yamlfmt a.yaml b.yaml c.yaml
   ```
   
- To beautify one or more files in the replace mode:

  ```bash
  yamlfmt -w a.yaml b.yaml c.yaml
  ```
  
- To beautify stdin and write to stdout:

  ```bash
  cat a.yaml | yamlfmt
  ```
  
- To beautify stdin and write to a file:

  ```bash
  cat a.yaml | yamlfmt > b.yaml
  ```
