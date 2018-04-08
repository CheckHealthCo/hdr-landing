## hdr-landing [![Build Status](https://travis-ci.org/CheckHealthCo/hdr-landing.svg?branch=master)](https://travis-ci.org/CheckHealthCo/hdr-landing)

### Getting Started

To use this theme:

*Step 1:* Clone this repo to your computer

```bash
git clone git@github.com:checkhealthco/hdr-landing.git
```

*Step 2:* Run `gem install bundler; bundle install` inside the new `/hdr-landing/` folder that was just created to install the required ruby dependencies.

*Step 3:* Build the site

- Build the site: `rake build` Note that this will clean before building the site

*Step 4:* Publish your site
Specifically for this project:

- `cp .sample.env .env`
- Fill in `.env` with production variables related to AWS S3 bucket
- Push the site with: `rake publish`

### Notes:

- Using travis to publish the site on build success

- Use the variables in .env file to fill in the env variables at travis-ci

### License

MIT. See LICENSE file in repo.
