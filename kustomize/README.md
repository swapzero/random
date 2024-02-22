
### Prereqs
- kustomize (I used v5.3.0)

### Run
```
kustomize build .
```
### Template replacing
- JSON template (as an annotation)
  ```json
      {
        "Type": "redirect",
        "RedirectConfig": {
          "Protocol": "#{protocol}",
          "Port": "#{port}",
          "Integer": ||BLA||,
          "Host": ||DOMAIN||",
          "Path": "/#{path}",
          "Query": "#{query}",
          "StatusCode": ||STATUS_CODE||"
        }
      }
  ```
- see components/replace-in-json-text.yaml for the logic (and some explanations)
