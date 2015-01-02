ErlPortTest
===========

This is just an example for me and whoever else needs it for using erlport and Elixir.

So far I just added the erlport library to my dependencies
  ```elixir
  {:erlport, github: "hdima/erlport"}
  ```

And then tried calling it in iex:

```elixir
iex(11)> {:ok, p} = :python.start()
{:ok, #PID<0.116.0>}
iex(12)> result = :python.call(p, :sys, :"version_info.__str__", [])
"sys.version_info(major=2, minor=7, micro=9, releaselevel='final', serial=0)"
iex(13)> result = :python.call(p, :operator, :add, [2,2])
4
iex(14)> :python.stop(p)
:ok
iex(15)>
```
