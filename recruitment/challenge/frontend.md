# USThing Recruitment Test (Frontend)
## Introduction
In this test, you will build a profile update form. You may ask for pre-completed modules to skip stages. You maybe search for reference freely during the test
## Requirements
- Your form request for existing profile 
- Form consists of itsc, name, email, age, website

## Resources
- GET / PUT profile page: `https://api.myjson.com/bins/18iw4x`
- How to access the api: `http://myjson.com/api`

## Checkpoints
1. Get json from profile api
2. Fill in the form with the json
3. Validate the form fields on submit
    - itsc cannot be changed
    - name cannot be empty
    - email must contain '@'
    - age must be > 0 and < 200
4. Pass the form to profile api with PUT method

## Bonus
- Code cleanliness and readability
- Use themes like Boostrap, semantic-ui, Foundation
- Use js ecosystem like jQuery, ReactJs
