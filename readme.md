# Address Seeker



searchers a website or a string for a us postal address and parses it.



## Installation



`pip install addr_seeker`



## Usage


 

### searching a string for an address

```python
from addr_seeker import AddrSeeker
s = SomeText
result = AddrSeeker.scanText(s)
print(result)
```
#### output:
(STREET, POBOX, CITY, STATE, ZIPCODE)
### searching a website for a postal address
```python
from addr_seeker import AddrSeeker
seeker = AddrSeeker(maxDepth= 2 ) 
#max tree depth to look, where the initial url is the root. 
	#0 means look only at the url page itself. 1 means look at the url and in all links in that page and so on
seeker.setUrl("www.apple.com")
result = seeker.findMailingAddr() 
print(result)
```
#### output:
`(3, ('1 infinite loop', None, 'cupertino', 'ca', '95014'), 1)`

result is in the following format:
	(STATUSCODE, (STREET, POBOX, CITY, STATE, ZIPCODE), DEPTH)


STATUSCODE:

0: page does not exist

1: branches do not exist

2: addr does not exist in neither the page nor it`s branches

3: addr found in tree

DEPTH is the depth of where the address was found








## Contributing




1. Fork it!

2. Create your feature branch: git checkout -b my-new-feature

3. Commit your changes: `git commit -am 'Add some feature'
4. Push to the branch: `git push origin my-new-feature
5. Submit a pull request :D

## Credits


Sherif Ewis

## License


The MIT License (MIT)
Copyright (c) 2014 Sherif Ewis

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


## Contact
sheri_eweis@hotmail.com.

