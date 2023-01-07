# ASCII-FIER

### Turn any image into ASCII! It's customizable and extremely easy to use!

# Before you download:

This program requires the `PIP` package installer and the `PIL` library. **Make sure you have both installed.**

#### PIP (https://pip.pypa.io/en/stable/):

Go to https://bootstrap.pypa.io/get-pip.py on the page press CTR/COMMAND+A to select everything and paste it into a .py file by calling it `get-pip.py`.

CD into the directory that you have the get-pip.py file in via terminal, and run `python get-pip.py`. If that doesn't work, try `py get-pip.py` and make sure you have Python 3 or higher.

#### PILLOW (https://pillow.readthedocs.io/en/stable/index.html):

Pillow needs PIP to install. Run: `python3 -m pip install --upgrade pip` and `python3 -m pip install --upgrade Pillow`.

# Installation

Unzip the file into the ASCII-FIER folder.

Open ASCII-FIER.py with a text editor and change the file directory so it lands on `image.png` in the ASCIi-FIER folder.

```python
# Open image file *MAKE SURE THE FILE PATH USES '/' AND NOT '\'*
filename = "image.png"
filepath = "C:/Users/[username]/Downloads/ASCII-FIER/image.png"
```

# Setup & Customization

There must be an image.[filetype] in the ASCII-FIER folder.

If you wish for it to use one of the jpeg formats, simply change it with the `png` after both `filename` and `filepath`.

If the image is too large to fit on the screen, or too small to have much detail, you can resize it before converting it to ASCII art here:

```python
    image = image.resize((int(width * 0.08), int(height * 0.08)))
```

Just play around with the `(width * 0.08)` and `(height * 0.08)` numbers until you find something that fits you.

One thing to keep in mind is that because of the way no characters can be completely square unless you change the line spacing, the ASCII will look higher than the original image. This varies everywhere.

To make sure it's exactly how you want, it's important to play around with the step size.

If the ASCII art is hard to read, you can try using a smaller step size when mapping pixel values to characters.

```python
            ascii_art += chr(ord('A') + pixel // 8)
```

The step size is the number at the end, which is currently set to '8'.

You can also try using a different character set to represent the pixel values (currently set to 'A')

You can use characters from ' ' (space) to '~' instead of 'A' to 'Z'.

###### oh yeah and some of this was made using openai
