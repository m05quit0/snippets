[В начало](README.md)

# Flask

#### Изменить mimetype ответа
```Python
@app.route('/robots.txt')
def robots():
    return render_template('robots.txt'), {'Content-Type': 'text/plain'}
```
