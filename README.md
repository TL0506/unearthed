# WEB103 Lab - *UnEarthed*

Submitted by: **Tiffany Lin**



## Video Walkthrough

**Note: please be sure to show the unique URL of each detail view in your walkthrough.**

Here's a walkthrough of implemented required features:

Loom Link because GIF thing didn't work

Loom Link: 
https://www.loom.com/share/c5f499be981a492b9be89b8b39cf8173

## Notes

- **Styling:** This app is styled with **custom CSS** ([client/src/style.css](client/src/style.css)) rather than Picocss, so that requirement is left unchecked. Swapping in Picocss would mean linking its CDN stylesheet and adjusting the custom rules.
- **Architecture:** The project is split into a `client/` (Vite + vanilla JS) and a `server/` (Express). `npm run build` in `client/` outputs the static site into `server/public/`. During development, run the API (`node server.js` in `server/`) and the Vite dev server (`npm run dev` in `client/`) at the same time — the Vite config proxies `/gifts` to `http://localhost:3001`.
- **Detail routes:** Each gift's detail view lives at a unique URL like `/gifts/1`, `/gifts/2`, etc., served by the Express route in [server/routes/gifts.js](server/routes/gifts.js).
- **Challenge:** A recurring source of confusion was stale Vite warnings and orphaned dev-server processes lingering on port 5173 after data changes — resolved by fully killing old Node processes and restarting both servers cleanly.

## Lab 2

Here's a walkthrough of Lab 2 features:

![Lab 2 Walkthrough](lab2.gif)

## Lab 3

Here's walkthrough of lab 3:
![Lab 3 Walkthrough](lab3.gif)

## License

    Copyright 2026 Tiffany Lin

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
