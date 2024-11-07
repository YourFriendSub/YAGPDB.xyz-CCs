<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Markdown in HTML</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: auto;
            padding: 20px;
        }
        h1, h2, h3, h4, h5, h6 {
            margin-top: 20px;
            font-weight: bold;
        }
        p, ul, ol, pre, code, blockquote {
            margin-bottom: 20px;
        }
        code {
            background-color: #f4f4f4;
            padding: 3px 6px;
            font-family: Consolas, monospace;
            font-size: 0.95em;
        }
        pre {
            background-color: #f4f4f4;
            padding: 15px;
            overflow: auto;
            font-family: Consolas, monospace;
        }
        blockquote {
            border-left: 4px solid #ccc;
            padding-left: 15px;
            color: #666;
            font-style: italic;
        }
        ul, ol {
            padding-left: 20px;
        }
        table {
            border-collapse: collapse;
            width: 100%;
            margin-bottom: 20px;
        }
        table, th, td {
            border: 1px solid #ddd;
            padding: 8px;
        }
        th {
            background-color: #f4f4f4;
        }
        img {
            max-width: 100%;
        }
        .task-list-item {
            list-style-type: none;
        }
        .task-list-item input {
            margin-right: 10px;
        }
    </style>
</head>
<body>

    <h1>Markdown to HTML Example</h1>

    <h2>Headers</h2>
    <h1>Header 1</h1>
    <h2>Header 2</h2>
    <h3>Header 3</h3>
    <h4>Header 4</h4>
    <h5>Header 5</h5>
    <h6>Header 6</h6>

    <h2>Emphasis</h2>
    <p>This is <strong>bold text</strong> and this is <em>italic text</em>.</p>
    <p>You can also <strong><em>combine bold and italic</em></strong>.</p>

    <h2>Lists</h2>
    <h3>Unordered List</h3>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3
            <ul>
                <li>Sub-item 1</li>
                <li>Sub-item 2</li>
            </ul>
        </li>
    </ul>

    <h3>Ordered List</h3>
    <ol>
        <li>First item</li>
        <li>Second item</li>
        <li>Third item</li>
    </ol>

    <h3>Task List</h3>
    <ul>
        <li class="task-list-item"><input type="checkbox" checked> Completed Task</li>
        <li class="task-list-item"><input type="checkbox"> Incomplete Task</li>
    </ul>

    <h2>Links</h2>
    <p>This is a <a href="https://www.example.com">link to example.com</a>.</p>

    <h2>Images</h2>
    <p><img src="https://via.placeholder.com/150" alt="Example Image"></p>

    <h2>Code</h2>
    <p>Inline code: <code>console.log("Hello, World!");</code></p>
    <h3>Code Block</h3>
    <pre><code>
// This is a code block
function greet() {
    console.log("Hello, World!");
}
greet();
    </code></pre>

    <h2>Blockquotes</h2>
    <blockquote>This is a blockquote. It can be used to highlight text, especially quotations.</blockquote>

    <h2>Tables</h2>
    <table>
        <thead>
            <tr>
                <th>Header 1</th>
                <th>Header 2</th>
                <th>Header 3</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Row 1, Column 1</td>
                <td>Row 1, Column 2</td>
                <td>Row 1, Column 3</td>
            </tr>
            <tr>
                <td>Row 2, Column 1</td>
                <td>Row 2, Column 2</td>
                <td>Row 2, Column 3</td>
            </tr>
        </tbody>
    </table>

    <h2>Horizontal Rule</h2>
    <hr>

    <h2>Escaping Characters</h2>
    <p>To display a literal asterisk (*), use a backslash: <code>\*</code>.</p>

</body>
</html>
