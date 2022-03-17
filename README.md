# envoy-tools
Tooling for debuging envoy

## update\_includes.sh

Using QtCreator's code model: 
  * Switch off clangd: Menu "Help" -> "About Plugins ..." type "ClangCodeModel" in the filter and make sure the checkbox in the "Load" column is unchecked. (If is checked, unchecked and restart QtCreator).
  * Import envoy using "File" -> "New File or Project", in the top level list select "Import Project", in the center list "Import Existing Project", click "Choose...", name the project "Envoy" (with a cap. "E"!!!) and point it to your existing source code. On the next page choose most of the directories and finalized the import by finishing the dialog.
  * Clone this repo or retrieve the `update_includes.sh` bash file and link or store it into the source directory of envoy.
  * Execute the `update_includes.sh` file (when you choose a different name for the project above, supply it to the script appending `.includes` to it).

The script adds a lot of paths to the already known ones from the build-directories. It does so using path's relative to the source directory.

This works fine with the internal code model of QtCreator. It is untested for using clangd or ClangCodeModel or other IDEs or language servers.

