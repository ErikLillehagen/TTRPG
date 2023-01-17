<%*
	const fileTypes = ['Game Log', 'DM Note', 'Misc']
	const campaigns = [{name: 'Queenslab Campaign 1'}]
	tp.file.

	const fileType = await tp.system.suggester(fileTypes, fileTypes)

	const createGameLogFile = () => {
		const game = await tp.system.suggester(games, games)
	}
	const createDmNoteFile = () => {
		new Notice('Not implemented')
	}
	const createDmNoteFile = () => {
		new Notice('Not implemented')
	}



-%>



<%*
 let qcFileName = await tp.system.prompt("Note Title")
 titleName = qcFileName + " " + tp.date.now("YYYY-MM-DD")
 await tp.file.rename(titleName)
 await tp.file.move("/Notes/" + titleName);
 -%>


<% tp.file.cursor() %>
