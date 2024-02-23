### Product Review and Ratting 

```mermaid
flowchart TD
    A[Product] -->|Post Reviews| B(Reviews)
    
    B-->|Like| D[LIKE]
    B -->|Dislike| E[Dislike]
    B -->|Mark helpfull| F[Mark helpfull]
    B -->|Reply| G[Reply]
    G -->|Reply| H[Reply]
```


### Film and  category

```mermaid
flowchart TD
    
        A(Film) <--> |Film-ID| B(Film-Actor) 
    
    B(Film-Actor) <--> |Actor-ID| c[Actor] 
     
    

    D(category) <--> |category-ID| E(Film-category) 
     
   A(Film) <--> |Film-ID| E(Film-category) 
 
```