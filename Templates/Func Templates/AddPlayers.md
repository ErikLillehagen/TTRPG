<%*
	const members = ['Artus', 'Avloppsmannen', 'Bhaxan', 'Gagurr', 'Moss', 'Neeve', 'Oogwai', 'Tuppis', 'Tylvi', 'Volkur'];
	
	const removeFromCurrent = (selected) => {
		const index = currentMembers.indexOf(selected);
		if (index > -1) {
			currentMembers.splice(index, 1);
		} 
	}
	
	const finalize = () => {
		if (selectedMembers.length > 0) {
			const result = selectedMembers.sort().join(', ');
			tR += result
		}
		selectedMembers = []
	}
	
	const currentMembers = members;
	let selectedMembers = []
	try{
		while (currentMembers.length > 0) {
			const selected = await tp.system.suggester(members, members,true, "Select players, esc to abort");
			removeFromCurrent(selected);
			selectedMembers.push(selected);
		}
		finalize();
	} catch {
		finalize();
	}

-%>