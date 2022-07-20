# sockpuppet


You probably want [this](https://github.com/eficode/wait-for) or [this](https://github.com/vishnubob/wait-for-it).

This is nice and succinct:

```bash
until nc -z $HOST $PORT; do sleep 1; done;
```

Even this may suffice:

```bash
until 2>/dev/null >/dev/tcp/{service}/{port}
do
    echo "-- {service} is not available.  Sleeping ..."
    sleep 2
done
```
