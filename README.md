# Rblx-Lua-Syntax-Highlighting-XML-XSHD-
A simple roblox Lua syntax highlighting using ICSharpCode's TextEditor in C#

To use this file, head to https://github.com/icsharpcode/SharpDevelop/wiki/Syntax-highlighting and use their provider for the TextEditor.

Once you have their text editor, use the following code to attach the syntax highlighting:

```cs
string dir = @"resources\highlighting\\"; // Insert the path to your xshd-files.
FileSyntaxModeProvider fsmProvider; // Provider
if (Directory.Exists(dir))
{
    fsmProvider = new FileSyntaxModeProvider(dir); // Create new provider with the highlighting directory.
    HighlightingManager.Manager.AddSyntaxModeFileProvider(fsmProvider); // Attach to the text editor.
    txtSQL.SetHighlighting("YourHighlighting"); // Activate the highlighting, use the name from the SyntaxDefinition node.
}
```
