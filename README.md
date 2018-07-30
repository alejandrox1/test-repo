# CI/CD Playground

## Commits
If you want to keep an eye on commits:
```
switch e := event.(type) {                                                  
case *github.PushEvent:                                                     
    if e.Ref != nil {                                                       
        fmt.Printf("%s:\n", *e.Ref)                                         
        for _, commit := range e.Commits {                                  
            msg := fmt.Sprintf("%s\n%s\n\tBy: %s\n\n", *commit.ID, *commit.Message, *commit.Author.Name)
            fmt.Println(msg)                                                
        }                                                                   
    }                                                                       
}
```
will more or less give you a `git log` like output.
