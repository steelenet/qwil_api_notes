# qwil_api_notes
Notes about the Qwil API

API Guide:
* Tells the user to specify a version (version=v1), the API user should not have to specify the version and get the latest version of the API if not specified.

API Docs:
* No need to include auth in each example (all are Basic auth, so it can be stated once and assumed).
* Mixing underscores and dashes is an odd style choice.
* api-token-auth_create
  * Request and response samples are the same.
  * Although being sent over HTTPS, sending the email and password as part of the body is a bad idea.
  * The response I received in testing did not include a token. I suspect this is because my account is not verified yet. If this is the intended behavior, then the user should simply receive a message back from the API saying they will not get a token until their account has been verified.

Website:
* I was able to turn off the modal preventing the user from interacting with their account before being verified and disable the blurring.
* Proof: http://jumpbox.live/qwil_001.png
* Doesn't seem to be any verification of what kind of documents are being sent to the system. I assume this occurs manually.