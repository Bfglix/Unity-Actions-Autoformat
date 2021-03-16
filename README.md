# Unity Auto Format 🔎

This action can be used to auto format the scripts in your Unity project! Making it easier to work with others with different formatting. I'm active on Github so pull requests and issues are welcome!

This action is built on top of the work of others, so a big thank you to `andstor/file-existence-action@v1.0.1`, `andstor/file-existence-action@v1.0.1`, and @shiena for the gist to build off of!

Here's the original gist → https://gist.github.com/shiena/197f949bc513858a85883d5529730310

## Usage

Unfortunately Github composite actions do not support uses yet. Meaning, at the time of writing this, basically only shell scripts can be run from composite actions. So instead you can find a full workflow in [`example-workflow.yml`](example-workflow.yml).

Simply copy the contents from there and paste them into a new workflow in your repository.

## Change Log
* March 16th 2021 - For some reason the workflow was failing, likely due to a change in another action being used. I updated the workflow for reliability. It now relies on less Actions and instead just formats using `dotnet format ./pathToScripts --folder` right in the shell, then checks for changes, and commits & pushes if so.
