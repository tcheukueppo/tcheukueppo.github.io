# ima.image

## Image(\*\*kwargs)

Create a new `Image` object.

**key-value arguments are:**

- `url`: Link to the site from which image links are going to be extracted.
- `subject`: Set space separated list of token use for scoring an extracted image.
- `timeout`: Connection Timeout, default value is 10 seconds.

## Methods

### Setters

`set_url(self, url)`

Link to the site from which image links are going to be extracted.

## Class Methods

1. `get_links(self, n, **kwargs)`

Navigate and return a generator of dictionaries describing the extracted `img` tags.

**key-value arguments are:**

- `min_score`: A positive integer, it is the minimum score an image should have.
You can plug-in a custom function which computes the score of an image based on your
own policy. Ima has a default static method in the `Image` class, it computes and
return the number of common tokens found between the contents of the `alt` attribute
and that of `self.subject`. The higher the returned value, the greater the number of
changes that the image is actually what you want but this is however not always true.

- `score_with`: Custom function for scoring an image. It is going to be invoked
with two arguments passed to it: first argument is `self.subject` and second is the content of
the `alt` attribute of the `img` tag in question.

- `use_content`: Tell `Image` object to ignore all `img` tags with no `alt` attribute.

Yielded dictionaries contain the following keys:

1. `url`: Image url.
2. `content`: If exists, contains the content of the image's `alt` attribute otherwise it is `None`.
3. `score`: The computed score, based on `content`.
4. `mime_type`: Mimetype of the image.

2. `download(self, **kwargs)`

Use this to iterate over images and download them.

**key-value arguments:**

- `rate`: Download rate, set the number of bytes to retrieve per iteration on the file to be downloaded.
- `overwrite`: Set to `True` to overwrite files that already exist.
- `path`: Path to the downloaded images
- `auto`: Set to `True` to auto generate a new name if another file with the same as the file
to be downloaded already exist in filesystem.

3. `download_from(self, link, **kwargs)`

`link` can either be a url or a dict yielded by `self.get_links(...)`.

It has the same key-value arguments as that of `self.download` with the following:

- `filename`: Preferred name of the image to be download.
