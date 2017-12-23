# Habitat

[Habitat](https://www.habitat.sh/)

# Running Morgue as Habitat Services

* MySQL server
* Apache
* PHP

`sudo hab sup run`

`sudo mkdir -p /hab/svc/mysql`

Create `/hab/svc/mysql/user.toml`

Can you use handlebars in the user.toml?  

bind should be set to `hostname -i`

```
root_password = "secret"
app_username = "morgue"
app_password = "morgue_password"
bind = "172.31.31.240"
```

`sudo hab sup start core/mysql`


Application:

init should create the database
