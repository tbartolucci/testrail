testrail
--------

testrail is a Go client library for accessing the [TestRail](http://www.gurock.com/testrail/) API

References
----------

Example usage
-------------

```
  package main

  import "github.com/educlos/testrail"

  func main(){

    username := os.Getenv("TESTRAIL_USERNAME")
    password := os.Getenv("TESTRAIL_TOKEN")

    client := testrail.NewClient("https://example.testrail.com", username, password)

    projectID := 1
    suiteID := 11
    cases, err := client.GetCases(projectID, suiteID)

    for _, c := range cases{
      fmt.Println(c.ID)
    }
  }
```


License
-------

MIT
