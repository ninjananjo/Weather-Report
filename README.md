# Weather-Report

The project's goal is to create and distribute weather reports for various locations.

### How to run

The report was created in IBM Data Studio. The IBM project details are required so the script can save and read objects.

```python
project = Project(project_id='', project_access_token='')
pc = project.project_context
```

Set up an account on [Weatherstack](https://weatherstack.com/) and add your key

```python
key = '' # Weatherstack key
```

Choose your locations and dates for the report. The dates are set up to include all days in the week.

```python
dates = week_days
locations = ['Glasgow, UK', 'Birmingham, UK', 'London, UK', 'Belfast'] # Choose locations
```

The email distribution is set up via Gmail. You will need to allow less secure apps on your account [instructions here](https://support.google.com/accounts/answer/6010255). Then put your email address in the 'fromaddr' and create a distribution list.

```python
fromaddr = "" # From email
toaddresses = [""] # Recipient list
```

Then schedule the report to run daily. I used the in-built IBM Data Studio scheduler.

## Authors

* **James Nanji** - [ninjananjo](https://github.com/ninjananjo)
