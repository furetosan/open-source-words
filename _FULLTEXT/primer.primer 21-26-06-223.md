primer primer is the design system that powers github primer includes 23 packages that are grouped into 3 core meta packages for easy install each package and meta package is independently versioned and distributed via npm so its easy to include all or part of primer within your own project packages the primer repo is managed as a monorepo that is composed of many npm packages core packages package version primer includes all 23 packages primer core primer product primer marketing install this repository is distributed with npm after installing npm you can install primer with this command sh npm install save primer usage the source files included are written in sass scss after installing with npm you can add your projects node modules directory to your sass include paths aka load paths in ruby then import it like this scss import primer index scss you can import individual primer modules by installing them with npm for instance sh npm install save primer navigation then you would import the module with scss import primer navigation index scss or while youre figuring out which modules you need you can import them directly from the primer modules directory like so scss import primer modules primer navigation index css build for a compiled css version of this module an npm script is included that will output a css version to build build css the built css file is also included in the npm package sh npm run build releasing staff only you can find docs about our release process in releasing md documentation you can read more about primer in the docs license mit © github