# :tada: Stacks

Stacks is a initiave to have differents **kinds** of runtimes for different types of projects. 

The idea is based on the experience of having used [buildpacks](https://buildpacks.io/) with cloudfoundry. 

For example this repo starts with datascience. It has `jupyter lab`, `pandas` and other tools.

Some images could be used entirely doing `docker run <image_name>` or as a base for a newer image. 

When possible services run with the non-root user `app`, so if you want to add packages you will need to create a `Dockerfile` use the
`root` user and install theese packages. 

If some package is founded to be a very common dependency, for instance in datascience stack I add vim because is a runtime for development purpose, reach me out and I can 
add new packages to the image it self. 


## Scaffolding

[Folders are namespaces](https://blog.golang.org/package-names). 

Each subfolder from here will have their own dependency managment. Mostly Python, Go and Javascript.

Each project could have their own structure, because sometimes I could use the subfolder as a kickstarter project. 
Usually they follow a pattern:

- a Makefile with some semantics `install`, `build`, `docker` and `release`
- linting specific tools
- ignore files
- `data`, `notebooks` folfers. 
- Some libraries configurations like `alembic` for sqlalchemy in the python world. 

### Ignore files

Some projects could be private, so please pay attention on the `.gitignore` file in the root of this project. 

Usually each environment starts with a `.gitignore` built usint the [topal tool](https://www.toptal.com/developers/gitignore) but custom files and folder could be added.

Also I try to add a broad of differents IDEs in the mix. Feel free to add whatever IDE that you considerer. 

## About this repo

This is a meta repo, a galaxy (?) to find differents stacks.

## Contribution

Feel free to suggest changes through issues. 

Also for commit message I'm using emojis following [this guide](https://gitmoji.dev/)

## License

All the work is done with a [Apache 2.0 license](LICENSE.md). 

## Disclaimer

I'm not a native english speaker, I would like more sites to clarify this to avoid misslearnings. 
So feel free to fix any grammar or error that you could found here, I try my best. 
