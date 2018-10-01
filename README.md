# Description

I'd like to understand why `model.constructor.name` is not available in prod builds
while it works in dev and test envs.

To reproduce

- `ember serve`
- `open http://localhost:4200`

You should see:

```
model.constructor.name: ArticleModel
model.constructor.modelName: article
```

Now stop the server and start it again in prod env

- `ember serve --environment production`
- `open http://localhost:4200`

You should see something like this:

```
model.constructor.name: n
model.constructor.modelName: article
```
