# Infowrap seed generator

The Infowrap Seed Generator creates seeds based on information in the database. By default all accounts in the database will be added to the seed. Alternatively, a wrap identifier may be specified, which will limit the seed to only that wrap's account's content and minimal information about other wraps that are referenced, to ensure the integrity of the seed.


## Usage

The Infowrap Seed Generator is built into the [api.infowrap.com](https://github.com/BizBuilt/api.infowrap.com) repository. You must download the repository and follow its setup instructions before using the seeder.

The following commands must be run from within the api.infowrap.com project folder on your system.

Generated seeds will be stored under the "api.infowrap.com" respository "tmp" folder.


### Command

	bundle exec rake infowrap:genseed[seed_name,target]

- `seed_name` - this determines the name of the folder this seed's data will be stored in
- `target` - optional Wrap ID or identifier to limit the content generated for the seed


### Examples

Generate a seed containing all content in the database:

	bundle exec rake infowrap:genseed[myseed]

Generate a seed containing only Jane Doe's content:

	bundle exec rake infowrap:genseed[jane_doe_seed,jane_doe]
