## Get started

Cloning the app and installing the dependencies...

```bash
git clone https://github.com/Vaibhav-Kulkarni-4/score-board-in-svelte.git
cd score-board-in-svelte
npm install
```

...then to serve the app, start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000) on your browser. You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.


## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).

### More info 

To get supplementary knowledge on svelte js, head to [svelte.dev](https://svelte.dev/)

To clone a project template in svelte app, go to [Svelte Project Template](https://github.com/sveltejs/template)
