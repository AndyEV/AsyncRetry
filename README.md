# Async Retry
Asynchronous retry in just 4 lines

```
public async Task<T> RetryAsync<T>(Func<Task<T>> func, int max 5)
{
    for (int i = 0; i < max; i++)
    {
        try { return await fun(); }
        catch { continue; }
    }
    return default;
}
```
