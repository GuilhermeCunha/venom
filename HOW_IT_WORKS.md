## How it works

We have 3 "layers" in our library: Store, Typescript Interface and WAPI.

1- Store: it is important to know that Whatsapp Web has a set of Javascript functions included in its [page] (https://web.whatsapp.com/), and we were able to reverse engineer access to these functions. That is, we do not use "clicks" on the screen to perform actions, all are executed through Whatsapp's own functions. Within our library, this obtainment of the functions can be found [here](https://github.com/orkestral/venom/blob/master/src/lib/wapi/store/get-store.js).

2- Typescript Interface: The user of the Venom library always uses this layer, it will be inside the project documentation, and has the responsibility to call the WAPI.

3- WAPI: This layer uses Pupperteer to perform the call to Store functions within the browser wave WhatsApp is running on.
