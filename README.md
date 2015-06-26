# HCron

Made a little utiltiy that will take a cronline as an argument or will attempt to read your crontab and translate it into something human readable. Most (read: all) of the heavy lifting is actually done by [prettycron](https://github.com/azza-bazoo/prettycron). 

## Usage:

```bash
hcron "0 11 * * * php awesomescript.php"
```

Will output
```
11:00 every day the process "php awesomescript.php" will run
```

Just executing `hcron` will read the output of "crontab -l | grep -v \#" (the grep -v part is to remove commented out cron jobs) and output all cronjobs in a human readable format.

## Installation:

### Through NPM:
npm install -g hcron

### Through git

Clone the repo to your home directory. Navigate to the directory & run:

```bash
sudo npm install
ln -s ~/hcron/bin/hcron /usr/local/bin/hcron
```
