# Wigan CAMRA Branch Constitution

The Wigan Campaign for Real Ale branch constitution and associated document
generation tools

## Document Generation

### Docker

#### PDF

Windows (Powershell)

``` sh
docker run --rm `
	--volume ${PWD}:/data pandoc/latex constitution.md `
	-o build/constitution.pdf
```

## Contributing

### Content Changes

### Style Guide

Keep lines to 80 characters in length, the following exceptions apply:

* Headings may exceed the 80 character limit.
* Tables and their contents may exceed the 80 character limit0
* Links may exceed the 80 character limit, but keep them on their own line.

### Authoring a Change

#### Command Line (Advanced Users)

1. First thing's first, check out a new branch with the following naming
		convention (_replacing *{name}* with a succinct name for your change):

		git fetch
		git pull
		git checkout -b feature/{name}

		A good example of a branch name might be:

		git checkout -b feature/v5.4.1

2. Make your change in `constitution.md`, changes should be small. Make small
	changes often.
3. "Stage" the change to your commit with `git add constitution.md`.
4. Check that the file has been staged with `git status`.
5. Commit your change with `git commit -m 'your commit message'`.
		
		Commit messages should be writen in the present tense (eg. "update" or
		"updates" rather than "updated")

		Commit messages should be succinct yet descriptive, eg:
		
		* Good message: 'update "17. Current branch officers": replace "Chair"'
		* Bad message: 'replace "Chair"'

6. Repeat steps 2 through to 5 as many times as required.
7. Push changes using `git push`, you may need to set the branch upstream.

### Publishing a Change

1. Create a "Pull Request" for your Git "branch", from your branch into `main`.
2. Ask Wigan CAMRA Branch members to review your change
3. Once you have approvals merge the pull request.
   1. Upon succesfully merging into the `main` branch document generation will
		be automatically executed and build artifacts created.