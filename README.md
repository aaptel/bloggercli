# bloggercli

Commandline interface to blogger to list, edit, post blog posts.

# Setup

## Python dependencies

You can install dependencies locally with virtualenv and pip:

    $ virtualenv-3.4 .virtenv
    $ .virtenv/bin/pip install -r requirements.txt

From there you can run bloggercli like so:

	$ .virtenv/bin/python bloggercli

## Google API key

You need your own Blogger API key for now. You need to request one on
Google API. You should get a `client_id.json` file at the end of the
process. Place it in the current directory.

During the first run a new tab will open in your browser where you
will be asked whether you want to let the app manage your blog and
given an authentication token. Follow the instructions and paste the
token in the terminal when asked. The result of this process will be
stored in a local file `credentials.dat` that will be reused the next
runs.

# Usage

Run with -h for help. Each subcommand (list/newpost/setpost/delpost) has it's own -h option.

Some sample calls:

    bloggercli -i BLOGID list
    bloggercli -i BLOGID newpost --draft --title "my title" ./my_html_content
    bloggercli -i BLOGID setpost --publish POSTID
    bloggercli -i BLOGID delpost POSTID
