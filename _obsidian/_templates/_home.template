<%*
const generateMOC = (folderChoicePath) => {
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
		
		const content = filesList.filter(f=>!!f).sort((a, b) => a.toLowerCase().localeCompare(b.toLowerCase())).join('')
	
		// insert the list of files in the active file
		tR+=content
	} else {
		new Notice(`Failed to create MOC for ${folderChoicePath}`, 5000);
	}
}
_%>

# What is this

This is an Obsidian Vault repository to store my notes.

## Notes

<%*
generateMOC("Notes/") 
%>


## Drawings

<%*
generateMOC("Drawings/") 
%>
