# HCron

Made a little utiltiy that will take a cronline as an argument or will attempt to read your crontab and translate it into something human readable. Most (read: all) of the heavy lifting is actually done by [prettycron](https://github.com/azza-bazoo/prettycron). 

## Usage:

```bash
hcron "0 11 * * * php awesomescript.php"
```

Will output
```
11:00 every day the process "php /var/www/lto/module/LtoEngine/jobs/ach-returns.php" will run
```

```bash
hcron
```
Will read the output of "crontab -l | grep -v \#" (the grep -v part is to remove commented out cron jobs) and output all cronjobs in a human readable format.
