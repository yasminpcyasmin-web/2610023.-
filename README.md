package main

import "fmt"
import "net/http"

func main() {
handlerIndex := func(w http.ResponseWriter, r *http.Request) {
fmt. Fprintln(w, "This is the About Page!")
}
http.HandleFunc("/", handlerIndex)

fmt.Println("server started at localhost:9011")
http.ListenAndServe(":9011", nil)

}
