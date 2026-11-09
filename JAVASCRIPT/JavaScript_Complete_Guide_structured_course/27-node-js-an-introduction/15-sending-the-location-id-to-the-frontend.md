# 27.15 — Sending the Location ID to the Frontend

> Section 27: Node.js: An Introduction

Now let's make sure the other route now also works. My goal is that users now actually get a link here which does not include all this information but just the ID which we generate on the server and then we output this link here with the ID and when we click the link or when we use the link, we reach that other route we defined here, this get route to then load this data for the ID. Now two things we need to do for that, for one we should send back the ID to the client so that on the client, we can encode it in the URL.

So here I'll generate my ID here and store it in a constant and then refer to this ID constant here and also send it back, maybe in a location or log ID field here in our response, that's important otherwise on the client, we can't generate a link with the ID in it. Then back to the client, we should take all this code which disables the button and so on into this then block so that this only happens once the data was sent to the server and we got a response and now here from data we need to get that ID, the location ID we get this from data.locId, why locId?

Well because on the response, we're sending this locId field, that's part of our JSON response, on the client we're parsing this JSON data, so we get an object which will have this locId field and now the location ID should be part of that URL. So we replace this part here with locId or location equals and now we inject the location ID here, so that now the link contains the ID instead of the full address data. So with that, we should restart our server side server so that we take our changes here into account and then go to the running frontend application, maybe search for a 6th avenue again, find that place and now you'll see we got this link with our location ID here.

Now let's make sure we also fetch that location by that ID with this URL, with this path on our backend server.

----------------------------------------
