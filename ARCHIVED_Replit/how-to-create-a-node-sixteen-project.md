# Step 1

Start by creating a Repl using the `Nix (Beta)` that is given when selecting the preferred language.

*Example:*

[<img src="https://github.com/itsjusttriz/faq/blob/main/replit/img/NixReplCreate.jpg" alt="Nix Repl Create">](https://github.com/itsjusttriz/faq/blob/main/replit/img/NixReplCreate.jpg)


# Step 2
Within this new Project, locate the file named `replit.nix`.
Inside this file, place the following:
<pre>
    <code style="font-family: monospace;">
        { pkgs }: {
            deps = [
                pkgs.nodejs-16_x
            ];
        }
    </code>
</pre>

# Step 3
> - Import/Paste your code to this project.<br />
> - Configure your `package.json` as you see fit.<br />
> - Keeping or Removing the default `README.md` file is completely your choice.<br />
(*But beware, some prewritten scripts already contain a default README and will replace this one.*)
> - Edit the `.replit` file to coincide with your configured `package.json` file.<br />
*Example:*<pre>run = npm start</pre>

# Step 4
Go to the `Shell` tab and run `npm i` to install the required dependencies for this project.

# Step 5
If you've configured the `.replit` file correctly, you should be free to click the green button, to run your project.