Plant Community LA Site

### Technologies used:

Based on https://github.com/surjithctly/neat-starter

- [Netlify CMS](https://www.netlifycms.org/)
- [Eleventy](https://www.11ty.dev/)
- [Alpine.js](https://github.com/alpinejs/alpine)
- [Tailwind CSS](https://tailwindcss.com/)

### How It works

Every commit to the main branch triggers a build on Netlify, which runs `npm run build` and then deploys the site. There is also an admin interface at /admin which is powered by Netlify CMS. Edits done through the Admin UI create GitHub commits. 

All content is stored as JSON inside the `src/_data` folder, so edits to the content can be made directly via Git/GitHub and we also get version control for all content on the site.

The site is deployed via Netlify as a 100% static site which makes it essentially free to run and very fast as there is no traditional database behind the site and everything sits in a CDN.

#### Admin

Our Admin UI is configured entirely via the file src/admin/config.yml. This is a pretty cool part of Netlify CMS, you can build the Admin UI entirely from Yaml and the UI is built on page load using their Admin framework, meaning the only 'backend' requirement for our site is the Netlify Admin script tag.


### Running the website locally

```
npm install
npm run build
npm start
```

Now open `http://localhost:8080` in your browser. Edits will reload the site, and edits to config.yml will reload the `/admin` UI.

### Opening Pull Requests

We welcome contributions to the site from the public. If you are going to spend a lot of time on a Pull Request, but aren't sure if your feature will be useful to us, feel free to open an Issue with your idea and get our feedback first. 
