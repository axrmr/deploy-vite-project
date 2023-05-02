# Vite template

This project was created with Vite. For familiarization and setting additional features [refer to documentation](https://vitejs.dev/guide/).

## Deploy

To set up a project deployment, you need to perform a few additional steps to set up your repository. Go to the `Settings` tab and in the `Actions` subsection select the `General` item.

![GitHub actions settings](./public/actions-config-step-1.png)

Scroll the page to the last section, in which make sure the options are selected as in the following image and click `Save`. Without these settings, the build will not have enough rights to automate the deployment process.

![GitHub actions settings](./public/actions-config-step-2.png)

The production version of the project will be automatically built and deployed to GitHub Pages, in the `gh-pages` branch, every time the `main` branch is updated. For example, after a direct push or an accepted pull request. 


```js
// https://vitejs.dev/config/
export default defineConfig({
  base: "/deploy-vite-project/", //name of your repository
  plugins: [react()],
});
```

Next, you need to go to the settings of the GitHub repository (`Settings` > `Pages`) and set the distribution of the production version of files from the `/root` folder of the `gh-pages` branch, if this was not done automatically.

![GitHub Pages settings](./public/repo-settings.png)
