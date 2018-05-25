# jquery-quicksearch with persist 201203*pike


Quicksearch filters html elements rowsusing a persistent text field

example usage:

	$('input#mysearch').quicksearch('#mytable tr',{
		'persist':true,
		'onBefore':function() {
			alert('foo')
		}
	});
	
options

	delay: 100,
	selector: null,						// a subselector for your jquery path
	stripeRows: null,					// array to apply striping on visible results
	loader: null,							// jquery path to a loading spinner
	noResults: '',						// jquery path to a no result message
	bind: 'keyup',						// event to use for persisting and filtering
	persist: false,						// wether to persist (sessionstorage)
	persist_key: '',					// element to add to persist key
	onBefore: function () { 
		return;									// what to do before filtering
	},
	onAfter: function () { 
		return;									// what to do after filtering
	},
	show: function () {	
		this.style.display = "";				// how to show stuff
	},
	hide: function () {
		this.style.display = "none";		// how to hide stuff
	},
	prepareQuery: function (val) {		// how to simplify queries
		return val.toLowerCase().split(' ');
	},
	
