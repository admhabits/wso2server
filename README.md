## GENERATE WSO2AM SERVER APIM WITH OKTETO

Prasyarat Memulai :

- **OKTETO CLI**.
- **Docker Compose**.
- **Kubernetes**

## Tutorial

- Deploy the **Polling App** on your personal namespace by clicking on the following button:

<p align="center">
<a href="https://cloud.okteto.com/deploy">
  <img src="https://okteto.com/develop-okteto.svg" alt="Develop on Okteto">
</a>
</p>

- To develop on the **frontend** component:

```
    $ okteto up -f frontend/okteto.yml
      ✓  Development container activated
      ✓  Files synchronized
         Namespace: githubid
         Name:      frontend
         Forward:   9229 -> 9229
                    8080 -> 80

    Welcome to your development environment. Happy coding!
    githubid:frontend okteto> yarn install
    githubid:frontend okteto> yarn start
```

- To develop on the **api** component:

```
    $ okteto up -f api/okteto.yml
      ✓  Development container activated
      ✓  Files synchronized
         Namespace: githubid
         Name:      api
         Forward:   5005 -> 5005
                    8080 -> 8080

    Welcome to your development environment. Happy coding!
    githubid:api okteto> mvn spring-boot:run
```