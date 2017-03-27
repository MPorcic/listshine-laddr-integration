# listshine-laddr-integration
A ListShine wrapper for laddr apps!

This wrapper enables you to add new contacts to a list on ListShine when they register for a new profile on your laddr app!
## Installation 
The path where each file should be is commented in the appropriate file.
  1. ListShine.php  
     -This file should be added to /php-classes/RemoteSystems directory of your site
  2. ListShineApi.php  
     -This file should be added to /php-classes/ListShine/ directory of your site
  3. Listshine.conf.php  
     -This file should be added to /php-config/RemoteSystems directory of your site
  4. listshine.php  
    Not to be confused with the above class ListShine.php add this file to:  
     /event-handlers/People/RegistretationRequestHandler/registerComplete/ 


In order to enable the checkbox that will add your subscribers, you will need to add this snippet in your registration template:
```
{if RemoteSystems\ListShine::$api_key}
                    <div class="checkbox">
                        <label>
                            <input type="checkbox" id="Subscribe" name="Subscribe">I want to receive emails
                        </label>        
                    </div>
{/if}
```

In order to sucessfully add the subscribers you need to do two things:
  1. Add your ListShine API key in the Listshine.conf.php file.
  2. Add the UUID of the contactlist you want to use for subscribing the users in the listshine.php file
