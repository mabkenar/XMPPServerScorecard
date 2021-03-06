#  XMPP Server Scorecard


XMPP Server Scorecard, a leaderboard of top XMPP servers.

This is a fork of netlify/staticgen and it is still containing information about static site generators. Stay tuned for more updates.

An extensive data set about XMPP server software is on [Zash/XMPP-Features](https://github.com/Zash/XMPP-Features) page. 
However, **XMPP Server Scorecard** aims to provide information about user-facing XMPP **providers**, i.e., website that people use to make XMPP accounts.


## Contributing

Missing a XMPP server here? Just fork the repo and add your generator
as a `<name>.md` in the `source/projects` folder.

Make sure to follow the following rules:

*   **Static Site Generation:** No "flat-file CMSs" or similar tools. The program must be able to output a static website that can be hosted in places like Netlify, S3 or Github Pages.
*   **Open Source:** The generator must have a public repository on Github that we can link to and pull in stats from.
*   **Stick to the format:** Fill out all the same fields as the other static site generators in `source/projects`.
*   **Short description:** Keep all the details for the body text, keep the description for the overview page short and sweet.

## Running locally

XMPPServerScorecard is built with Middleman. To install and run locally:

    git clone https://github.com/mabkenar/XMPPServerScorecard.git
    cd XMPPServerScorecard
    bundle install
    bundle exec middleman

You'll run into GitHub's API limits very quickly if you just do this. To avoid this we recommend you create a Github API token with permissions to access public repositories and Gist.

Then create a Gist with a single file `data.json` with an empty javascript object literal as content: {}

Then set these environment variables before running middleman:

    export GITHUB_TOKEN=YOUR_TOKEN
    export GIST_ID=ID_OF_YOUR_GIST

Then middleman will use the Gist you specified to archive stats (stars, forks and issues) for the repositories.

## License
This project is licensed under the [MIT license](http://opensource.org/licenses/MIT).
