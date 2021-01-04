### Python flask框架

#### flask 重定向到https

```python
def https_redirect() -> Optional[Response]:
    if request.scheme == 'http':
        return redirect(url_for(request.endpoint,
                                _scheme='https',
                                _external=True),
                        HTTPStatus.PERMANENT_REDIRECT)
```

