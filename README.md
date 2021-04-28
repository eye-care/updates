
# NHS Eyes project
This is a prototype site constructed by various [folks](https://github.com/eye-care/updates/graphs/contributors) to show how a team might work more in the open.

## Running this site
Simply, this site is a Hugo site using the Doks templating system which is deployed to Netlify.

If you'd like to run the project locally, in a terminal, you'll want to run the following commands:

```bash
git clone git@github.com:eye-care/updates.git
```
This will clone this repository to your local environment.

```bash
npm install
```
This installs all the dependancies the site needs, as listed in package.json
If you don't already have npm installed, follow these instructions first to download and install [Node.js](https://nodejs.org/) (it includes npm) for your platform.

```bash
npm run start
```
This will start the server on your local system, and give you a local URL (most likely localhost:1313 but it may give you a different port if that one's already in use) you can open in your browser to view the site, and any changes you make locally.

## Project structure
As this is using the Doks system, it follows the basic layouts defined in that project and you may find that documentation helpful (see below), but for a basic orientation:
* Templates for the major layouts can be found here: https://github.com/eye-care/updates/tree/main/layouts
* Content that is displayed in those layouts is here: https://github.com/eye-care/updates/tree/main/content
* You can adjust the navigation elements here: https://github.com/eye-care/updates/blob/main/config/_default/menus.toml
* Style and visual elements can be edited here: https://github.com/eye-care/updates/tree/main/assets 

When a change is made to the site, and you have the project running locally (as above) or you push a change to the repository, triggering a netlify build, these files are combined and built to a directory within the resources directory call "gen".  This directory is never checked in to the repository and should never be manually edited - the files there will be overwritten whenever a change is made by the build steps - and to protect that from happening it's listed in the [.gitignore file](https://github.com/eye-care/updates/blob/main/.gitignore).

## Deployment

Whenever a change is made to this repo a build is automatically triggered at Netlify and will update the site found at: https://eyecare-updates.netlify.app/  Similarly, if you make a pull request to this repo, Netlify will create a "[deployment preview](https://docs.netlify.com/site-deploys/overview/#branches-and-deploys)" where you can preview the changes made before merging the pull request. No other steps are required to deploy the site. 

If you want to change the URL for the netlify site, change DNS records to point a different domain to the site, or otherwise make changes to the Netlify settings, speak to [@techforevil](https://github.com/techforevil) who has the login credentials.  You can also create a new netlify account and deploy this same repository there, if needs be. 

## Documentation

- [Netlify](https://docs.netlify.com/)
- [Hugo](https://gohugo.io/documentation/)
- [Doks](https://getdoks.org/)

## Communities

- [Netlify Community](https://community.netlify.com/)
- [Hugo Forums](https://discourse.gohugo.io/)
- [Doks Discussions](https://github.com/h-enk/doks/discussions)

