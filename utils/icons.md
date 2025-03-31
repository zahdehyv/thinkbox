```dataviewjs
// codeblock language should be dataviewjs

/**
 * List all icons available to `obsidian.setIcon()`
 * 
 * @author Unxok <me@unxok.com>  
 * 
 * Based on the original work from:
 * @author Ljavuras <ljavuras.py@gmail.com>
 * @link https://gist.github.com/ljavuras/28095f04113fda73f7dc4efcc776b94f
 */

dv.container.createEl("style", { attr: { scope: "" }, text: `
.icon-table {
    display: flex;
    flex-wrap: wrap;
    margin: 0 var(--size-4-6);
}

.icon-item {
    padding: var(--size-4-2);
    line-height: 0;
    cursor: pointer;
}

.icon-item:hover {
    background-color: var(--background-modifier-active-hover);
    border-radius: var(--radius-s);
}
`});

let lucide_ids = [];
let other_ids = [];

dv.container.createEl("br");
const searchContainer = dv.container.createDiv({cls: "search-input-container"});
const inp = searchContainer.createEl('input', {type: 'search'})
const clearBtn = searchContainer.createDiv({cls: "search-input-clear-button"})
dv.container.createEl("br");

const container = dv.container.createEl('div')

const updateResults = (val) => {
	container.empty();
	if (!val) {
		renderIconTable(lucide_ids, 'lucide');
		renderIconTable(other_ids, 'other');
		return;
	}
	const lucide = lucide_ids.filter(id => id.includes(val));
	const other = other_ids.filter(id => id.includes(val));
	renderIconTable(lucide, 'lucide');
	renderIconTable(other, 'other');
}

inp.addEventListener('input', (e) => {
	const val = e.target.value;
	updateResults(val)
})

clearBtn.addEventListener('click', () => {
	// updateResults("");
	inp.value = "";
})

function renderIconTable(ids, label) {
	container.createDiv({text: `${ids.length} ${label} icons`})
    const tableEl = container.createDiv("icon-table");
    ids.forEach((id) => {
        let iconEl = tableEl.createDiv("icon-item");
        obsidian.setIcon(iconEl, id);
        obsidian.setTooltip(iconEl, id, { delay: 0 });
        iconEl.onclick = () => {
            navigator.clipboard.writeText(id);
            new Notice("Copied to clipboard.");
        }
    });
}

lucide_ids = obsidian.getIconIds()
    .filter(id => id.startsWith("lucide-"))
    .map(id => id.slice(7));
renderIconTable(lucide_ids, 'lucide');

other_ids = obsidian.getIconIds().filter(id => !id.startsWith("lucide-"));
renderIconTable(other_ids, 'other');
```
