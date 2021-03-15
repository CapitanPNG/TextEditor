<script>

const TYPES =
{
    "title"      :      "Titolo",
    "caption"    :  "Didascalia",
    "description": "Descrizione"
};

let editor    = null;
let fileInput = null;

function addInput (type)
{
    let input = document.createElement("input");

    input.classList.add(type);
    input.value = TYPES[type];

    editor.appendChild(input);

    input.focus();
}

function addTitle ()
{
    addInput("title");
}

function addCaption ()
{
    addInput("caption");
}

function addDescription ()
{
    addInput("description");
}

function addImage ()
{
    fileInput.click();
}

</script>

<svelte:head>
    <title>
        TextEditor
    </title>
</svelte:head>

<div class="text-editor">
    <div class="toolbar">
        <button
            on:click={addTitle}
        >
            Aggiungi Titolo
        </button>
        <button
            on:click={addCaption}
        >
            Aggiungi Didascalia
        </button>
        <button
            on:click={addDescription}
        >
            Aggiungi Descrizione
        </button>
        <button
            on:click={addImage}
        >
            Aggiungi Immagine

            <input
                bind:this={fileInput}

                type="file"
                accept="image/*"

                style="display: none;"
            >
        </button>
    </div>
    <div
        bind:this={editor}

        class="editor"
    ></div>
</div>

<style>

.text-editor {
    padding: 10px;
    width: 768px;
    height: inherit;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: #515151;
    background-color: #f0f0f0;
    border: 1px solid #ececec;
}

.toolbar {
    padding: 10px;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}

.editor {
    width: 100%;
    display: block;
    flex-grow: 1;
    background-color: #fbfbfb;
}

:global(input) {
    width: 100%;
    padding: 10px 16px;
    display: table;
    background-color: transparent;
    border: none;
}

:global(.title) {
    font-size: 36px;
    font-weight: 500;
}

:global(.caption)
{
    font-size: 18px;
    font-weight: 400;
}

:global(.description) {
    font-size: 14px;
    font-weight: 400;
}

</style>