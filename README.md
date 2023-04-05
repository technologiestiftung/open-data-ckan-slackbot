![](https://img.shields.io/badge/Built%20with%20%E2%9D%A4%EF%B8%8F-at%20Technologiestiftung%20Berlin-blue)

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-2-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

# Open Data CKAN Slackbot

This is a netlify function for a Slackbot that queries the CKAN API of [Berlin's data portal](https://daten.berlin.de) for new datasets and for updated datasets. It's written in TypeScript, using the Bolt JS framework.
It can be triggered via specific keywords in Slack messages. Also, it responds to the slash command /opendata [number of days] and then displays the new and updated records for the queried number of days.

## Prerequisites

- [Netlify](https://www.netlify.com) Account
- [Slack](https://slack.com/intl/de-de/) Account and Workspace

## Installation

* Run `npm install` to install all node dependencies.
* Install Netlify CLI globally using the command `npm install netlify-dev -g`.
* To run this function locally, you'll need to link your Netlify site with your repository. Easiest way is to create a `.netlify` folder and inside that, create a `state.json` file with the following contents. Get your site id or API id from the site settings and paste it here. Then run the command `netlify link`.
```json
{
	"siteId": "PASTE YOUR API ID HERE"
}
```
* Run `netlify build` to build your code and generate a function. This command uses the settings in the `netlify.toml` file to run a build command. The build command compiles TypeScript files into JavaScript and automatically creates the required `netlify/functions` folder for you and places the `index.js` function file inside this folder. 
* Run `netlify dev` to start a local development server to test your function. If the local server starts at port 8888, then the URL to access this function is `http://localhost:8888/.netlify/functions/index`.

## Usage or Deployment

There are several steps necessary to get the Slackbot running.

- deploy the function to netlify
- integrate Slack by creating a Slack app, grabbing the credentials and integrating it into the function so that the function can communicate with the Slack app
- configure the slack app to subscribe to events and to implement the slash command

All this steps are described in the Medium article ["Creating a Slack Bot Using Netlify Functions"](https://levelup.gitconnected.com/creating-a-slack-bot-using-netlify-functions-465d2a981686) by Clyde D'Souza. You can follow the tutorial to get the app running and to deploy it.

## Contributing

Before you create a pull request, write an issue so we can discuss your changes.

## Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/Lisa-Stubert"><img src="https://avatars.githubusercontent.com/u/61182572?v=4?s=64" width="64px;" alt="Lisa-Stubert"/><br /><sub><b>Lisa-Stubert</b></sub></a><br /><a href="https://github.com/technologiestiftung/template-default/commits?author=Lisa-Stubert" title="Documentation">📖</a> <a href="https://github.com/technologiestiftung/template-default/commits?author=Lisa-Stubert" title="Code">💻</a> <a href="#ideas-Lisa-Stubert" title="Ideas, Planning, & Feedback">🤔</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://fabianmoronzirfas.me/"><img src="https://avatars.githubusercontent.com/u/315106?v=4?s=64" width="64px;" alt="Fabian Morón Zirfas"/><br /><sub><b>Fabian Morón Zirfas</b></sub></a><br /><a href="#mentoring-ff6347" title="Mentoring">🧑‍🏫</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

## Credits

<table>
  <tr>
    <td>
      <a href="https://odis-berlin.de">
        <br />
        <br />
        <img width="200" src="https://logos.citylab-berlin.org/logo-odis-berlin.svg" />
      </a>
    </td>
    <td>
      Together with: <a href="https://citylab-berlin.org/en/start/">
        <br />
        <br />
        <img width="200" src="https://logos.citylab-berlin.org/logo-citylab-berlin.svg" />
      </a>
    </td>
    <td>
      A project by: <a href="https://www.technologiestiftung-berlin.de/en/">
        <br />
        <br />
        <img width="150" src="https://logos.citylab-berlin.org/logo-technologiestiftung-berlin-en.svg" />
      </a>
    </td>
    <td>
      Supported by: <a href="https://www.berlin.de/sen/inneres/">
        <br />
        <br />
        <img width="100" src="https://logos.citylab-berlin.org/logo-berlin-seninnds-en.svg" />
      </a>
    </td>
  </tr>
</table>

