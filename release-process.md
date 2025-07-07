## Model development

Up until the first release, models should be developed in a private repository. By convention these repositories should have a `-dev` suffix, e.g. `OccamResearchLtd/occam-model-dev`.

To create a new R package repo, you can use the [occam-package-template](https://github.com/OccamResearchLtd/occam-package-template).

## Making a model public
When ready for release, the following steps should be followed:

1. In the dev repo, create a release branch from `main` (e.g. `release/v1.0.0`):
	```
	git checkout -b release/v1.0.0
	```

1. Create an archived copy of all files in the release branch:
	```
	git archive --format zip --output /full/path/release-v1.0.0.zip release/v1.0.0
	```

1. Extract the archived files to a new directory (e.g. `occam-model`):
	```
	unzip /full/path/release-v1.0.0.zip -d /full/path/occam-model
	```

1. Initialise a new Git repository in the extracted directory:
	```	
	cd /full/path/occam-model
	git init
	git branch -M main
	git add .
	git commit -m "Initial public release v1.0.0"
	```


1. Create a new private repository in the OccamResearchLtd GitHub organisation (e.g. `OccamResearchLtd/occam-model`). This will be made public after a final manual review.

1. Push your new local repository to this new GitHub repository:
	```
	git remote add origin git@github.com:OccamResearchLtd/occam-model.git
	git push -u origin main	
	```

1. Final internal review by other team members:
	1. Review the code and documentation in the new repository.
	1. Ensure all sensitive information has been removed or anonymised.
	1. Ensure correct license file is included, and usage guidelines are clearly documented in the `README.md` file.

	If there are any issues found during the review, they should be addressed in the `release/v1.0.0` branch of the dev repository. Once resolved, repeat the steps from 1 to 7.

1. Make the new repository public, and create a release on GitHub:
	1. Go to the repository on GitHub.
	1. Click on "Releases" in the sidebar.
	1. Click "Draft a new release".
	1. Set the tag version (e.g. `v1.0.0`).
	1. Add a title and description for the release.
	1. Click "Publish release".

## Adding a DOI

Follow the [GitHub instructions](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content#issuing-a-persistent-identifier-for-your-repository-with-zenodo) to create a DOI using Zenodo.

Once the DOI is created, it should be added to the `README.md` file of the public repository, and to the release notes.
