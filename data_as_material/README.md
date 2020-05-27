# Infinity Quine
### By Ervin Baccay

![](https://github.com/ebaccay/art_w23ac/blob/master/data_as_material/quine.png)

## Explanation

I wanted to do something on the abstract "number" of infinity. Ever since high school, I've been particularly obsessed with the
concept of infinity. Because of this, the number that I was going to creatively interpret is infinity.

An art style that I'm particularly interested in is pixel art and I was originally going to create the infinity symbol in 
pain-staking detail using pixel art. However, the more that I thought about this idea, the more I realized that pixel art has 
nothing to do with infinity. I wanted the medium to convey the concept more than just showing a symbol.

Because of this, I decided to go towards ASCII art. This is infinitely more interesting than pixel art and connects more to 
the assignment as well. Looking through the text document of ASCII art just shows a jumble of text that has no meaning. 
However, by literally looking at the big picture, an image is revealed. The original intent of the data is no longer just for
humans to read or machines to parse, it's for humans to ignore the smaller details and instead take in the image that is the
whole.

Despite the leap from pixel art to ASCII art, I still felt that I could do more. I still wanted the artwork to somehow be
infinite. The final piece of the puzzle came to me when I thought of [quines](https://en.wikipedia.org/wiki/Quine_(computing)).
Quines are programs that output itself whenever run. By using quines, the artwork itself not only visually looks like an 
infinity symbol but _acts_ infinite as well. The original text is no longer meaningless on a small scale but is now meaningful.

By running the command `python infinity_quine.py > infinity_quine.txt`, this recreats the contents of `infinity_quine.py` into
the new file `infinity_quine.txt`. Then, by setting the boundaries of `infinity_quine.txt` to be 500 characters wide, the image
of infinity appears. Also by just running `python infinity_quine.py`, the entire program is revealed. The code is not
just outputting the contents of itself in order, but rather algorithmically _reconstructing_ itself in an infinite loop.

## How I Did It
1) Sketch an infinity symbol on my iPad and transfer to my computer. This original drawing is `infinity_pre.png`
2) Use [this website](https://www.text-image.com/convert/ascii.html) to convert this image into ASCII. A width of 500 
characters was used.
3) Using the code found [here](https://codegolf.stackexchange.com/questions/118373/print-a-quine-that-contains-the-input),  I 
then created `quinify.py` in order to create the quine version of the artwork.
4) Run `python quinify.py > infinity_quine.py` in order to create the actual quine file which is `infinity_quine.py`.
5) Run `python infinity_quine.py > test_quine.py` to replicate the program.
6) Running `python infinity_quine.py` or `python test_quine.py` will output the same thing!

*Note*: I had to change all non-alphabet characters in the original ASCII art to alphabet characters in order to actually get
the quine to work. I also padded space on the right side of the image for the same purpose. To view the image, you must set
your text editor to only have 500 characters per line otherwise the entire image will blend together and look bad.
