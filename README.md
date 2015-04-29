# fest
Files backed up rESTfully

````
{
    "name": "my_backup",
    "timestamp": "1985-10-26T21:45:00",
    "base": "/var/www/edgiese.com/public"
    "omit": ["tmp/*", ".git/*"],
    "files": {
        "./index.php": {
            "hash": "1234567890ABCDEF1234567890ABCDEF12345678",
            "timestamp": "2015-04-15T00:00:00+0000",
            "availability": -1,
            "user":"iansltx",
            "group":"iansltx",
            "permissions":777
        },
        "./subdir/blah.php": {
            "hash": "1234567890ABCDEF1234567890ABCDEF12345678",
            "timestamp": "2015-04-15T00:00:00+0000",
            "availablility": 0,
            "user":"edgiese",
            "group":"apache",
            "permissions":644
        }
    },    "omit": ["tmp/*", ".git/*"],

    "directories": {
        "./subdir": {
            "timestamp": "2015-04-15T00:00:00+0000",
            "user":"edgiese",
            "group":"apache",
            "permissions":644
        }
    }
}
````

## Add a manifest
````
POST /manifests
````

## Get lists of available manifests
````
GET /manifests
````

## Get a single manifest
````
GET /manifests/name/<name>
````

## Get a file
````
GET /files/a123b1234
````

##Put a file
````
PUT /files/a123b1234
````
