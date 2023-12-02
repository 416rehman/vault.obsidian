<%*

	let file = tp.file.find_tfile("_Sidebar");  
	if (file) {
		let contents = await tp.file.include("[[_sidebar.template]]");
		await this.app.vault.modify(file, contents);
	}


	file = tp.file.find_tfile("Home");
	if (file) {
		contents = await tp.file.include("[[_home.template]]");
		await this.app.vault.modify(file, contents)
	}

%>
