### Seed Data

Feel free to create your own named directories in the 'infowrap' directory with your own preferred seed file.
Example Usage from within api.infowrap.com:

***Note: Always run this first before seeding:***

```
rake db:drop; rake db:create; rake db:migrate
```

Then seed:

```
bundle exec rake infowrap:seed['/Users/nathan/Documents/seed/infowrap/nathan/seed.json',true]
```

Sample JSON seed.json file:

```json
{
  "name":"Nathan Walker",
  "accounts":[
    {
      "name":"Nathan",
      "login":"nathan",
      "password":"mario1",
      "email":"nathan.walker@infowrap.com",
      "wraps":[
        {
          "name":"Nathan",
          "identifier":"nathan",
          "public":true,
          "featured":true,
          "contacts":[
            {
              "name":"Personal",
              "data":[
                {
                  "name":"Email",
                  "value":"nathan.walker@infowrap.com"
                },
                {
                  "name":"Phone",
                  "value":"(503) 810-6104"
                }
              ]
            }
          ],
          "about":[
            {
              "name":"Links",
              "content":"www.apple.com"
            }
          ]
        }
      ]
    }
  ]
}
```
