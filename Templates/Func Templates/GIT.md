<%*
	try {
		let msg = await tp.system.prompt("Commit message", "", true);
		if(!msg) msg = `Manual save at ${tp.date.now("YYYY-MM-DD_HH:mm:ss")}`;
		new Notice(`Comitted with message: ${msg}`);

		const root = app.vault.adapter.getBasePath().replace(/(\s)/g, '\\$1');
		const c = await tp.user.gcp({root, msg});
		new Notice(c)
	} catch(e) {
		new Notice('Aborted!')
	}
-%>