# qwil_api_notes
Notes about the Qwil API

API Guide:
* Tells the user to specify a version (version=v1). Verison should be optional and the users gets the latest version of the API if not specified.

API Docs:
* No need to include auth in each example (all are Basic auth, so it can be stated once and assumed).
* Mixing underscores and dashes is an odd style choice.
* Most of the notes seem 
* api-token-auth_create
  * Request and response samples are the same.
  * Although being sent over HTTPS, sending the email and password as part of the body is a bad idea.
  * Although not a verified user, I am still able to get a token back from the API. Unclear if this is intended behavior or if the user should simply receive a message back from the API saying they will not get a token until their account has been verified.
* Other API response examples also do not include anything that resembles a real response
* api-token-revoke_create
  * Oddly worded description
* bank_search
  * bank_search_list
    * No description of this endpoint
    * Not sure if there is a need to list every possible currency. Give a few as examples and either link to or provided an expanded list if the user wants to see all currencies.
    * Same thing applies to country.
    

Website:
* I was able to turn off the modal preventing the user from interacting with their account before being verified and disable the blurring.
* Proof: http://jumpbox.live/qwil_001.png
* Doesn't seem to be any verification of what kind of documents are being sent to the system. I assume this occurs manually.