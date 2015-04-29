# fest
Files backed up rESTfully

````
{
    "name": "my_backup",
    "base": "/var/www/edgiese.com/public"
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
        
    ],
    "omit": ["tmp/*", ".git/*"],
    "private": ["configuration.php"] 
}
````

## Add a manifest
````
POST /manifests
````
## Let lists of available manifests

GET /manifests
GET /manifests/name/my_backup
GET /manifests/id/012345ABC
GET /manifests/latest
GET /files?hash=a123b123,b123c123,d123e343&format=gz
GET /files/a123b1234
PUT /files/a123b1234
