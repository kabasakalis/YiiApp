# Yii App v.2.0.0
By [Spiros Kabasakalis](http://iws.kabasakalis.gr/)

## Overview

Yii Project Template with Bootstrap layouts and Bootswatch color skins.
## [Live Demo](http://yiiapp.kabasakalis.tk)

## Features (so far)

- Six Bootstrap v3.0.0 layouts (as found in [Bootstrap v3.0.0 example docs](http://getbootstrap.com/getting-started/#examples)
- Six Bootstrap v2.3.2 layouts (as found in [Bootstrap v2.3.2 example docs](http://getbootstrap.com/2.3.2/getting-started.html#examples)
- [Bootswatch](http://bootswatch.com/) color skins.
- Usage of [Password Strategy Extension](http://www.yiiframework.com/extension/yii-password-strategies/).
- Password Reset with email verification.
- Registration with email activation.
- Delete inactive Users (users that registered but did not activate their account) within a configured period of time,
  (default is one day).This is done with a console command,which can be ran as cron job.See commands folder.
- [ReCaptcha](http://www.google.com/recaptcha) for antispam,(optionally).
- [Input Extension](http://www.yiiframework.com/extension/input/),for data sanitation.
- [YiiStrap](http://www.getyiistrap.com/) and [YiiWheels](http://yiiwheels.2amigos.us/).These two library extensions rely on v2.3.2 Bootstrap.


## Set it up
- Clone the git repo ```git clone git://github.com/drumaddict/YiiApp.git`` - or [download it](https://github.com/drumaddict/YiiApp/archive/master.zip)
- Specify your local development domain in index.php,(constant LOCAL_DOMAIN) so that the configuration file can differentiate between local and production environment.For example,you can fill in database info for both environments and the script will figure it out,assuming your virtual host does'nt have the same domain name as your real host.
- Hook up your Yii framework path in index.php,(both local and live on server).
- Fill in database info in config/main.php and config/console.php.(both local and live on server).
- Fill in your recaptcha private and public keys in config/main.php,if you want to use [recaptcha](http://www.google.com/recaptcha).
- Fill in myEmail and gmail_password  parameters in config/main.php in order to use Gmail SMPT server
  for email.To set up your localhost (in my case XAMPP stack) to send emails with Gmail SMPT Server,(for testing purposes),
  see this [article](http://expertester.wordpress.com/2010/07/07/how-to-send-email-from-xampp-php/).
- Run the migration in migrations folder,or use the sql dump in data folder to create the user table and a couple of test users.
  (Manually set the status active (1) and remove the activation_key entry for test users.)

## Changing theme,layout and color skin.
- By default the app uses Bootstrap v.3.0.0,if you want to use v.2.3.2 (you may want to use 2.3.2 if you also use Yiistrap/YiiWheels),you must set ```'theme'=>'bootstrap2``` in ```config\main.php```.
- Set the layout at the application level in ```config\main.php```,``` 'layout' => '[LAYOUT]',```
- Available layouts for Bootstrap v2.3.2 :starter,hero,fluid,carousel,justified-nav,marketing-narrow.
- Available layouts for Bootstrap v3.0.0 :starter-template,offcanvas,carousel,justified-nav,jumbotron,jumbotron-narrow.
- In ```config\main.php```,in params array fill in ```'bootswatch2_skin'=>'[SKIN NAME]'``` if you use Bootstrap v2.3.2 or```'bootswatch3_skin'=>'[SKIN NAME]'``` if you use v3.0.0.
- Available values for ```bootswatch2_skin```: none (default bootstrap colors),amelia,cerulean,cosmo,cyborg,flatly,journal,readable,simplex,slate,spacelab,spruce,superhero,united.
- Available values for ```bootswatch3_skin```: none (default bootstrap colors),amelia,cerulean,cosmo,cyborg,flatly,journal,readable,simplex,slate,spacelab,united.
- In ```config\main.php```,in params array,set ```'render_switch_form'=>true``` if you want to render a form for changing layouts and skins.(For Bootstrap v3.0.0 only).

## RESOURCES

- [Bootstrap](http://getbootstrap.com/)
- [Bootstrap v3.0.0 example docs](http://getbootstrap.com/getting-started/#examples)
- [Bootstrap v2.3.2 example docs](http://getbootstrap.com/2.3.2/getting-started.html#examples)
- [Bootswatch](http://bootswatch.com/)
- [Password Strategy Extension](http://www.yiiframework.com/extension/yii-password-strategies/)
- [Input Extension](http://www.yiiframework.com/extension/input/)
- [mailer](http://www.yiiframework.com/extension/mailer/)
- [YiiStrap](http://www.getyiistrap.com/)
- [YiiWheels](http://yiiwheels.2amigos.us/)
