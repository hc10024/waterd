# MNWD water usage optimization

## app

http://bit.ly/mnwd_forecast

Data lives in the Dropbox and can be accessed locally or remotely.

### Local test environment set up for development

Add the following lines to your ~/.Renviron (create ~/.Renviron if needed).

    MNWD_ENV=test
    MNWD_DATA_DIR=/path/to/your/Dropbox/mnwd_dk/Data

### Server setup

As `sudo su shiny`, add the following to ~/.Renviron.

    MNWD_ENV=prod
    MNWD_DATA_DIR=/srv/shiny-server/data

### Promoting a model to production

In local (test) mode your models should be pushed to `$MNWD_DATA_DIR/models/<username>`. To promote a model to produciton simply copy the model over to `$MNWD_DATA_DIR/models`, and make sure you add the needed metadata to the `MODEL_LIST` object in `app/common.R`.

## Wiki

https://github.com/fwhigh/waterd/wiki 

## Storage constraint math

![Alt text](/../master/math_picture/contraint_math.PNG?raw=true "Chris's storage math")
