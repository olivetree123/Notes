# HTTP参数解析

#### 转成对象

```
type New_User struct {
    Name string `json:"name"`
    Job  string `json:"job"`
}

func AddUser(w http.ResponseWriter, r *http.Request) {
    var user New_User
    decoder := json.NewDecoder(r.Body)
    decoder.Decode(&user)
    fmt.Printf("%+v\n", user)
}
```

#### 转成 map
```
func AddUser(w http.ResponseWriter, r *http.Request) {
    params := make(map[string]interface{})
    decoder := json.NewDecoder(r.Body)
    decoder.Decode(&params)
    fmt.Printf("%+v\n", params)
    name := params.Get("name").(string)
    public := params.Get("public").(bool)
}
```