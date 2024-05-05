# Create a function locally using Core Tools

## Azure Functions Core Tools allow local function development

1. **Create a local Azure Functions project**:
   - Run `func init loan-wizard` from the root folder to create a functions project.
   - Select node as the worker runtime and javascript as the language.

2. **Create an HTTP-triggered function**:
   - Navigate to the new `loan-wizard` directory.
   - Run `func new` to start the function creation wizard.
   - Select HTTP trigger as the template and name the function `simple-interest`.
   - Open the Cloud Shell editor with `code .` and replace the contents of `simple-interest.js` with provided code snippet.

3. **Implement the simple-interest function**:
   - Replace the contents of `simple-interest.js` with provided JavaScript code snippet.
   - Save the file and close the editor.

4. **Run the function in Cloud Shell**:
   - Start the Functions host silently in the background with `func start &> ~/output.txt &`.
   - View the output log with `code ~/output.txt`.
   - Send an HTTP GET request to the locally running function without parameters using `curl "http://localhost:7071/api/simple-interest" -w "\n"`.
   - Send an HTTP GET request to the locally running function with parameters using `curl "http://localhost:7071/api/simple-interest?principal=5000&rate=.035&term=36" -w "\n"`.
   - View the output log again with `code ~/output.txt`.
