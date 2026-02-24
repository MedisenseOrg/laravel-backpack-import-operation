## Installation (Local Development)

### Method 1: Adding Repositories to composer.json

To use the package locally while developing, you can add the VCS repository configuration directly to your `composer.json` file. Here’s how to do it:

1. Open your `composer.json` file.
2. Add the following structure under the `repositories` section:
   
   ```json
   "repositories": [
       {
           "type": "vcs",
           "url": "path-to-your-local-repo"
       }
   ],
   ```
   
3. Replace "path-to-your-local-repo" with the path to your local package repository.
4. Add the package to the `require` section of `composer.json`:
   
   ```json
   "require": {
       "vendor/package-name": "dev-main"
   }
   ```

5. Run `composer update` to install the package.

### Method 2: Using the Composer Config Command

Alternatively, you can use the Composer command line to add a VCS repository configuration:

1. Navigate to your project directory.
2. Run the following command to add your local repository:
   
   ```bash
   composer config repositories.local vcs path-to-your-local-repo
   ```
   
3. After adding the repository, you can require the package by running:
   
   ```bash
   composer require vendor/package-name dev-main
   ```
   
4. This will fetch the package directly from your specified local path without needing to update the `composer.json` manually.

Following either of these methods will allow you to work with your package locally during development.