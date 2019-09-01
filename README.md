# qwil_api_notes
Notes about the Qwil API

API Guide:
* Tells the user to specify a version (version=v1). Verison should be optional and the users gets the latest version of the API if not specified. If a version is deemed necessary, as a style choice, I would like to see it included as part of the API call path for easy debugging. (ex: api.qwil.co/v1/billing)
* Guide would likely benefit from real world examples to help get developers going (copy + paste code to be run in a sandbox).
* Is there a sandbox? I see a reference to staging.qwil.co.
* Guide would benefit from telling a story or sample flows of how other companies use Qwil.

API Docs:
* No need to include auth in each example (all are Basic auth, so it can be stated once and assumed).
* Mixing underscores and dashes is an odd style choice.
* Most of the notes seem aimed at developers (which makes sense, but non-devs should be able to understand as well)
* Super users are mentioned several times throughout the docs without explanation. The endpoints should operate as described and authorization for various operations should be explained by API responses.
* Some over verbose naming in the endpoint list (ex: "The bank accounts for a specific Platform. Enables create, retrieve, update (PUT/PATCH), destroy, and list.). All endpoints should be simply and obviously named.
* If an endpoint does not require a body, say so.
* Not sure what "platform_pk" represents or how to use it (but it is referenced many times).
* Not every endpoint is explained (ex: healthz_cambridge_list)
* api-token-auth_create
  * Request and response samples are the same.
  * Although being sent over HTTPS, sending the email and password as part of the body is a bad idea.
  * Although not a verified user, I am still able to get a token back from the API. Unclear if this is intended behavior or if the user should simply receive a message back from the API saying they will not get a token until their account has been verified.
  * The token did not give me full access.
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