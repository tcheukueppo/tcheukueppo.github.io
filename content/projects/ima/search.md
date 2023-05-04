# ima.search

## Search(\*\*kwargs)

Create a new search object.

**key value arguments**:

- `engine`: Possible search engines are `google`, `duckduckgo`, and `yahoo`.
- `query`: Your search query
- `save`: Boolean value, if set to `True`, then search caches search results.
- `save_path`: Path to the directory that will contain the cache results, Defaults to your `$HOME`
directory.
- `timeout`: Connection Timeout, default value is 10 seconds.

## Methods

### Setters

1. `set_engine(self, str)`

Set a new engine, this changes url used to make the HTTP request.

2. `set_query(self, str)`

Change query, this also changes the url used to make the HTTP request.

### Class Methods

1. `next(self, as_image = Bool, save = `Bool`)`

Set `save` to `True` if you want to cache the results.

Navigate to the next page and return the result as a list of urls if `as_image`
is `False` otherwise, return a generator of `Image` objects.

2. `back(self, as_image = `Bool`, save = `Bool`)`

Set `save` to `True` if you want to cache the results.

Navigate to the previous page and return the result as a list of urls if `as_image`
is `False` otherwise, return a generator of `Image` objects.

3. `get_links(self, n, **kwargs)`

**Key-value arguments**:

- `save`: A boolean, set to `True` to cache search results.
- `start`: Tell search object to extract links as from the start of the page if `start`
is `True`, otherwise just extract by continuing from the current page.
- `as_image`: Set to `True` to return a generator of `Image` objects.

Navigate and get `n` links as a list of urls if `as_image` is `False` otherwise return
a list of image objects.

4. `query_saves(self, **kwargs)`

**Key-value arguments:**

- `query`: select cached search results whose query is exactly the value set to `query`
- `query_like`: select cached search results whose query matches the regular expression
set to `query_like`
- `frequency`: The frequency determines how many times results were cached.
So, use this parameter to select records whose frequency is the value in `frequency`.
