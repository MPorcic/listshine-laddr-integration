# listshine-laddr-integration
A ListShine wrapper for laddr apps!

This wrapper enables you to add new contacts to a list on ListShine when they register for a new profile on your laddr app!

The path where each file should be is commented in the appropriate file. 

In order to enable the checkbox that will add your subscribers, you will need to add this snippet in your registration template:

{if RemoteSystems\ListShine::$api_key}
                    <div class="checkbox">
                        <label>
                            <input type="checkbox" id="Subscribe" name="Subscribe">I want to receive emails
                        </label>        
                    </div>
{/if}

In order to sucessfully add the subscribers you need to do two things:
  1. Add your ListShine API key in the Listshine.conf.php file.
  2. Add the UUID of the contactlist you want to use for subscribing the users in the listshine.php file
