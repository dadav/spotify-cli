# spotify-cli
## usage
```bash
# play
spotify-cli --play

# next / prev
spotify-cli --next
spotify-cli --previous

# meta
spotify-cli --meta --meta-format "{artist} - {title}"

# open
spotify-cli --open <URL>
```

### polybar
you could also use it in your polybar like this
```ini
[module/spotify]
type = custom/script
label = "%{A1:spotify-cli --prev:}  %{A}%{A1:spotify-cli --toggle:}  %{A}%{A1:spotify-cli --next:}  %{A} %output%"
exec = spotify-cli --meta
exec-if = pgrep -x spotify
interval = 5
```
