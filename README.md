# Rust Tokenizer

A command-line tool for counting tokens in text using a BPE tokenizer, using [OpenAI's tiktoken](https://github.com/openai/tiktoken).

## Usage

```bash
tokenizer <tokenizer_filepath> <text_to_encode>
```

### Arguments
- `tokenizer_filepath`: Path to the tokenizer file containing base64-encoded token/rank pairs
- `text_to_encode`: The text you want to tokenize

### Example

```bash
tokenizer ./tokenizer.txt "Hello, world!"
```

Output:
```
Token count: 3
```


### Tokenizer File Format

The tokenizer file should contain base64-encoded token and rank pairs, one per line:
```
<base64_encoded_token> <rank>
<base64_encoded_token> <rank>
...
```

## License

MIT License

Copyright (c) 2022 OpenAI, Shantanu Jain

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
