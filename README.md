# terebra
Auto form validation and centralized ajax request


```const form = new terebra('#form-id', '.input-class', '.input-ignore', '#submit-btn-id');
				 form.fn_focus();
				 form.fn_oninput();
				 form.fn_click(function(e)
				 {
              form.active = function()
              {
                  //Callback function when request is active
              }
              form.done= function()
              {
                  //Callback function if executed
              }
              form.fail = function()
              {
                  //Callback function if fails
              }
              form.complete = function()
              {
                  //Callback function when done
              }


              let validated_data = form.fn_validate();
              if( validated_data )
              {
                  form.settings["url"] = site_url+"account/"+action+"/";
                  form.settings["data"] = validated_data;
                  form.fn_request();
              }
				 });
