# Web - Headers

We’re sent to a page that is blank. But looking at the headers we see this:

`eyJhbGciOiJIUzUxMiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJncm9kbm97MWZRRFE1c3dhaEdjVGNmMn0iLCJuYW1lIjoiSm9obiBEb2UiLCJpYXQiOjE1MTYyMzkwMjJ9.Prqxaq3rMHc1eOs7-n67mvW3h0Zmug3q417Rac3roqsQ6GA_cMsJDUEWybB4ixROTEsd3bLERJWQArD8CIuFpg`

JWT Token decode gives us this:

{ "sub": "grodno{1fQDQ5swahGcTcf2}", "name": "John Doe", "iat": 1516239022 }

The flag is grodno{1fQDQ5swahGcTcf2}
