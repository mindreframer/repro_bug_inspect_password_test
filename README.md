# ReproLivestreamBug



BUGS: 

Running tests from root: 


```bash
==> example
.......................................

  1) test inspect/2 for the User module does not include password (Example.AccountsTest)
     apps/example/test/example/accounts_test.exs:504
     Refute with =~ failed
     code:  refute inspect(%User{password: "123456"}) =~ "password: \"123456\""
     left:  "%Example.Accounts.User{__meta__: #Ecto.Schema.Metadata<:built, \"users\">, id: nil, email: nil, password: \"123456\", hashed_password: nil, confirmed_at: nil, inserted_at: nil, updated_at: nil}"
     right: "password: \"123456\""
     stacktrace:
       test/example/accounts_test.exs:505: (test)

........................................................................................
Finished in 0.7 seconds (0.3s async, 0.4s sync)
128 tests, 1 failure

```


Running tests from apps/example: 

```bash
$ mix test
................................................................................................................................
Finished in 0.7 seconds (0.3s async, 0.4s sync)
128 tests, 0 failures

Randomized with seed 679613
```

