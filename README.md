# One-time machine setup
## ruby
Download and install [ruby](https://www.ruby-lang.org/en/documentation/installation/) on your local computer.

## git
Download and install [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on your local computer.

I also hear the [github desktop](https://desktop.github.com/) tool is pretty nice on windows.

## github
Create an account on [github](https://github.com/).

Have sure Rae give you developer [Write access](https://docs.github.com/en/issues/planning-and-tracking-with-projects/managing-your-project/managing-access-to-your-projects#granting-a-collaborator-access-to-your-project) to the [SeattleLungProject Project](https://github.com/raesian/SeattleLungProject)

## SSH
Install [SSH](https://learn.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse?tabs=gui) on your local computer.

## ssh key
Generate an ssh key that you can associate with your github account. See [github's article](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) for more details.

## Clone the repository
`git clone git@github.com:raesian/SeattleLungProject.git`

## Initialize your dev environment
- Run `bundle install` - ensure it's successful

# How this website works
It runs on [github pages](https://pages.github.com/)

It uses [Jekyll](https://jekyllrb.com/) the static site generator.

## Publishing changes the the site
Any changes that are pushed to the `gh-pages` branch will go live on https://www.seattlelungproject.com/ .

## Basic Workflow
This workflow covers making changes on your local computer, verifying them, and pushing them to the live site.

1. Start the local jekyll server with `bundle exec jekyll serve --watch`
2. Note the "Server address: " line in the terminal output. Navigate to that URL in your web browser.
3. Make the modifications you want to make.
4. Ensure they look okay in your local browser.
5. Stage any changes you've made with `git add`.
6. Commit your staged changes with `git commit`
7. Once you're happy and want to go "live" you can `git push`

As a more "advanced" workflow, you could also push to another branch on github, and them merge that branch into `gh-pages` when it's ready.

## What these files are
| file/directory | purpose                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CNAME          | github pages's domain name management                                                                                                                                                    |
| _config.yml    | Stores configuration data for jekyll                                                                                                                                                     |
| css/           | CSS style sheets for the site                                                                                                                                                            |
| fonts/         | Fonts for the site                                                                                                                                                                       |
| img/           | Images for the site                                                                                                                                                                      |
| _includes/     | These are the partials that can be mixed and matched by your layouts and posts to facilitate reuse. See jekyll docs.                                                                     |
| index.html     | The main page of the website. Templated.                                                                                                                                                 |
| js/            | javascript for the site                                                                                                                                                                  |
| _layouts/      | These are the templates that wrap posts. See jekyll docs                                                                                                                                 |
| _posts/        | Your dynamic content. The naming convention of these files is important, and must follow the format: YEAR-MONTH-DAY-title.MARKUP. See jekyll docs.                                       |
| _site/         | This is where the generated site will be placed (by default) once Jekyll is done transforming it. It's probably a good idea to add this to your .gitignore file. Don't push to the site. |
