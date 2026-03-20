<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Tags Guide</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #4F46E5;
            --primary-hover: #4338CA;
            --bg-gradient-start: #1e3c72;
            --bg-gradient-end: #2a5298;
            --card-bg: #FFFFFF;
            --text-main: #1F2937;
            --text-muted: #6B7280;
            --border-color: #E5E7EB;
            --task-bg: #EEF2FF;
            --primary-light: #E0E7FF;
        }

        body {
            font-family: 'Inter', sans-serif;
            margin: 0;
            padding: 20px;
            background: linear-gradient(135deg, var(--bg-gradient-start) 0%, var(--bg-gradient-end) 100%);
            background-attachment: fixed;
            color: var(--text-main);
            line-height: 1.6;
        }

        .container {
            max-width: 900px;
            margin: 20px auto;
            padding: 40px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(10px);
        }

        h1 {
            text-align: center;
            color: var(--primary-color);
            margin-bottom: 40px;
            font-size: 2.8rem;
            font-weight: 700;
            border-bottom: 3px solid var(--primary-light);
            padding-bottom: 15px;
        }

        h2 {
            color: var(--text-main);
            margin-top: 40px;
            font-size: 1.8rem;
            font-weight: 600;
        }

        h5 {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-top: 20px;
            margin-bottom: 10px;
            font-weight: 500;
        }

        p {
            margin-bottom: 15px;
            font-size: 1.05rem;
        }

        .task-card {
            background-color: var(--task-bg);
            border-left: 6px solid var(--primary-color);
            border-radius: 10px;
            padding: 20px 25px;
            margin: 25px 0;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .task-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
        }

        .task-badge {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            font-size: 0.85rem;
            font-weight: 600;
            padding: 5px 10px;
            border-radius: 6px;
            margin-bottom: 12px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
            padding: 2px 4px;
            border-radius: 4px;
            transition: background-color 0.2s ease;
        }

        a:hover {
            background-color: var(--primary-light);
            text-decoration: none;
        }

        code {
            background-color: #F1F5F9;
            padding: 4px 8px;
            border-radius: 6px;
            font-family: 'Courier New', Courier, monospace;
            color: #E11D48;
            font-weight: 600;
        }

        ul, ol, dl {
            margin-left: 20px;
            margin-bottom: 20px;
            background: #F8FAFC;
            padding: 20px 40px;
            border-radius: 10px;
            border: 1px solid var(--border-color);
        }

        li {
            margin-bottom: 10px;
            font-size: 1.05rem;
        }

        dt {
            font-weight: 700;
            margin-top: 15px;
            color: var(--text-main);
            font-size: 1.1rem;
        }

        dd {
            margin-left: 0;
            padding-left: 20px;
            border-left: 3px solid var(--primary-light);
            color: var(--text-muted);
            margin-top: 8px;
            margin-bottom: 20px;
        }

        /* Form Styling */
        form {
            background: white;
            padding: 30px;
            border: 1px solid var(--border-color);
            border-radius: 12px;
            margin-top: 20px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
        }

        .form-row {
            display: flex;
            gap: 20px;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 20px;
            flex: 1;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--text-main);
        }

        input[type="text"],
        input[type="date"],
        textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s ease, box-shadow 0.3s ease;
            box-sizing: border-box;
        }

        input[type="text"]:focus,
        input[type="date"]:focus,
        textarea:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px var(--primary-light);
        }

        textarea {
            resize: vertical;
            min-height: 100px;
        }

        .radio-group {
            display: flex;
            gap: 20px;
            padding: 10px 0;
        }

        .radio-label {
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: normal;
            cursor: pointer;
        }

        .button-group {
            display: flex;
            gap: 15px;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid var(--border-color);
        }

        button {
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.2s ease;
            flex: 1;
        }

        .btn-submit {
            background-color: var(--primary-color);
            color: white;
            flex: 2;
        }

        .btn-submit:hover {
            background-color: var(--primary-hover);
            transform: translateY(-1px);
        }

        .btn-clear {
            background-color: #F3F4F6;
            color: var(--text-main);
            border: 1px solid var(--border-color);
        }

        .btn-clear:hover {
            background-color: #E5E7EB;
        }

        .btn-cancel {
            background-color: #FEF2F2;
            color: #DC2626;
            border: 1px solid #FECACA;
        }

        .btn-cancel:hover {
            background-color: #FEE2E2;
        }

        footer {
            text-align: center;
            margin-top: 50px;
            padding-top: 30px;
            border-top: 2px solid var(--border-color);
            color: var(--text-muted);
            font-size: 0.95rem;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>HTML Tags Guide</h1>

        <h2>The <code>&lt;a&gt;</code> Tag</h2>
        <p>The <code>&lt;a&gt;</code> tag is used to create a hyperlink that connects a webpage to another section on the same webpage, or to another webpage, or allows one to upload or download a file. A hyperlink can be text, an image, a video, etc.</p>
        
        <h5>General syntax of a tag</h5>
        <div class="task-card">
            <code>&lt;a href="destination"&gt;target destination&lt;/a&gt;</code>
        </div>

        <div class="task-card">
            <span class="task-badge">Task</span>
            <p>Create a link that when clicked will take the user to the HTML documentation on the <code>&lt;a&gt;</code> tag. The link name should be "HTML TAGS".</p>
            <p><strong>Solution:</strong> <a href="https://html.com" target="_blank">HTML TAGS</a></p>
        </div>

        <h2>HTML Lists</h2>
        <p>A list is a sequence of items arranged in a particular order; it can be horizontal or vertical. HTML lists organize content into either an <strong>ordered list</strong>, <strong>unordered list</strong>, or <strong>definition list</strong> to make information clear and easy to read.</p>
        
        <p><strong>Ordered list:</strong> A sequence of items labeled using numbers, letters, or Roman numerals.<br>
        <strong>Syntax:</strong></p>
        <code>
            &lt;ol&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;item1&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;item2&lt;/li&gt;<br>
            &lt;/ol&gt;
        </code>

        <div class="task-card">
            <span class="task-badge">Task</span>
            <p>Create a list of 5 common HTML tags (Ordered List):</p>
            <ol type="i">
               <li><code>&lt;a&gt;</code> tag</li>
               <li><code>&lt;form&gt;</code> tag</li>
               <li><code>&lt;table&gt;</code> tag</li>
               <li><code>&lt;div&gt;</code> tag</li>
               <li><code>&lt;img&gt;</code> tag</li>
            </ol>
        </div>

        <div class="task-card">
            <span class="task-badge">Task</span>
            <p>Create a list of my favorite HTML tags (Unordered List):</p>
            <ul style="list-style-type: square;">
               <li><code>&lt;abbr&gt;</code></li>
               <li><code>&lt;div&gt;</code></li>
               <li><code>&lt;link&gt;</code></li>
               <li><code>&lt;head&gt;</code></li>
            </ul>
        </div>

        <div class="task-card">
            <span class="task-badge">Task</span>
            <p>Create a definition list to describe Internet Application Programming:</p>
            <dl>
              <dt>Internet Application Programming</dt>
               <dd>The process of developing software applications that run on the internet or communicate over the internet.</dd>
            </dl>
        </div>

        <h2>HTML Forms</h2>
        <p>HTML forms are used to get input from the user for the web application. These inputs are processed by the business logic of the web app and maybe stored in the database.</p>

        <div class="task-card">
            <span class="task-badge">Task</span>
            <p>State a list of all the components/paths of HTML forms using a definition list:</p>
            <dl>
                <dt><code>&lt;form&gt;</code></dt>
                <dd>The container for all form elements. Attributes: <code>action</code> (URL to send data), <code>method</code> (HTTP method like GET/POST).</dd>
                
                <dt><code>&lt;input&gt;</code></dt>
                <dd>Used to create interactive controls for web-based forms. Attributes: <code>type</code>, <code>name</code>, <code>value</code>.</dd>
                
                <dt><code>&lt;label&gt;</code></dt>
                <dd>Defines a label for several form elements. Attributes: <code>for</code> (binds to an input's id).</dd>

                <dt><code>&lt;button&gt;</code></dt>
                <dd>A clickable button used to submit forms or cancel actions. Attributes: <code>type="submit"|"button"|"reset"</code>.</dd>
            </dl>
        </div>

        <div class="task-card">
            <span class="task-badge">Task</span>
            <p>Create a well-designed form to capture specific user data:</p>
            
            <form action="#" method="get">
                <div class="form-row">
                    <div class="form-group">
                        <label for="firstName">First Name</label>
                        <input type="text" id="firstName" name="firstName" placeholder="Enter first name" required>
                    </div>
                    <div class="form-group">
                        <label for="lastName">Last Name</label>
                        <input type="text" id="lastName" name="lastName" placeholder="Enter last name" required>
                    </div>
                </div>

                <div class="form-group">
                    <label for="dob">Date of Birth</label>
                    <input type="date" id="dob" name="dob" required>
                </div>

                <div class="form-group">
                    <label>Gender</label>
                    <div class="radio-group">
                        <label class="radio-label">
                            <input type="radio" name="gender" value="male" required> Male
                        </label>
                        <label class="radio-label">
                            <input type="radio" name="gender" value="female" required> Female
                        </label>
                    </div>
                </div>

                <div class="form-group">
                    <label for="opinion">Opinion on the phrase "Ubuntu"</label>
                    <textarea id="opinion" name="opinion" placeholder="Share your thoughts on 'I am because we are'..." required></textarea>
                </div>

                <div class="button-group">
                    <button type="reset" class="btn-clear">Clear Data</button>
                    <button type="button" class="btn-cancel">Cancel</button>
                    <button type="submit" class="btn-submit">Submit Form</button>
                </div>
            </form>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 HTML Guide. All rights reserved.</p>
    </footer>
</body>
</html>
