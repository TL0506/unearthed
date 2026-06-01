# WEB103 Project 1 - *UnEarthed*

Submitted by: **Tiffany Lin**

About this web app: **UnEarthed is a gift-discovery web app where you can browse a curated collection of unique gift ideas. Each gift shows its name, price point, and target audience on the home page, and clicking "Read More" opens a detailed view with the full description, who submitted it, and when. An Express API serves the gift data, and a vanilla-JavaScript frontend renders the home page, detail pages, and a custom 404 page.**

Time spent: **1** hours and **15** minutues 

## Required Features

The following **required** functionality is completed:

<!-- Make sure to check off completed functionality below -->
- [x] **The web app uses only HTML, CSS, and JavaScript without a frontend framework**
- [x] **The web app displays a title**
- [x] **The web app displays at least five unique list items, each with at least three displayed attributes (such as title, text, and image)**
- [x] **The user can click on each item in the list to see a detailed view of it, including all database fields**
  - [x] **Each detail view should be a unique endpoint, such as as `localhost:3000/bosses/crystalguardian` and `localhost:3000/mantislords`**
  - [ ] *Note: When showing this feature in the video walkthrough, please show the unique URL for each detailed view. We will not be able to give points if we cannot see the implementation* 
- [x] **The web app serves an appropriate 404 page when no matching route is defined**
- [ ] **The web app is styled using Picocss**

The following **optional** features are implemented:

- [x] The web app displays items in a unique format, such as cards rather than lists or animated list items

The following **additional** features are implemented:

- [x] A "Test" button in the header that intentionally navigates to an invalid route, making it easy to demo the 404 page
- [x] A persistent header (logo, app title, and Home button) generated dynamically with JavaScript across all pages
- [x] Express backend with a dedicated `/gifts` API route serving the gift data as JSON
- [x] Vite dev-server proxy so the frontend can call the `/gifts` API during development

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
