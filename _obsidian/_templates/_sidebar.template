## Drawings
<%*
// Check the folder specified below and build a list of all markdown files
// all files in subfolders will be included

// = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
// MacOS example
folderChoicePath = "Drawings/"
// If you are on Windows, try: "resources\health\"
// = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =

if (folderChoicePath != null) {
	new Notice(`Folder: ${folderChoicePath}`, 5000);
	let filesInFolder = new Array();
	console.log("folderChoicePath: " + `${folderChoicePath}`)
	filesInFolder =  app.vault.getMarkdownFiles().filter(file => {
		return file.path.includes(folderChoicePath)
	})
	const filesList = new Array();
	filesInFolder.forEach((file) => {
			filesList.push('\n - [[' + file.basename + ']]')
	});
	
	const content = filesList.sort((a, b) => a.toLowerCase().localeCompare(b.toLowerCase())).join('')

	// insert the list of files in the active file
	tR+=content
	new Notice(`Created new MOC`, 5000);	
} else {
	new Notice(`No folder selected`, 5000);
}
_%>
