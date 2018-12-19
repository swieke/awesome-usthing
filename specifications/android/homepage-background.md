# Feature Guideline: Remote-controlled Homepage Background Color :art: 

## Goal :checkered_flag: 
Allow the app's homepage color to be changed remotely :sparkles: 


## Resources :books: 
I have already setup endpoints for fetching the required data. :100: 
Values can be changed by us in the database, and can be fetch by performing `GET` call on:
`https://restdb.usthing.xyz/api/v2/db/_table/BackgroundColor`
:::info
Necessary API key are required in the request header, which is already available in our app
:::

The expected result is as follows:
```json
{
    "resource": [
        {
            "id": 0,
            "color": "#01579B"
        },
        {
            "id": 1,
            "color": "#79655D"
        }
    ]
}
```


## //TODO :pencil2: 
- Fetch the required result in the app everytime the app opens
- Store the two colors in app local storage
- Update the background color gradients from the two stored values
    - Currently the background gradient is already generated using two color values


Feel free to ask if you have any questions.
Happy Coding!
