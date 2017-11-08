# Utilities

- [Publishing](#publishing)
- [Updating](#updating)

Docweaver provides simple artisan utility to commands to assist with managing your product documentations. 

<a name="publishing"></a>
## Publishing

To publish documentation for a product you may use the `docweaver:publish` artisan command.

e.g. 
```bash
php artisan docweaver:publish "My Product" https://doc.repo.address.git 
```

This command pulls documentation for "My Product" from the specified public git repository. This will publish the `master` branch and each existing tag.

<a name="updating"></a>
## Updating

To update documentation for a product you may use the `docweaver:update` artisan command.

e.g. 
```bash
php artisan docweaver:update "My Product" 
```

This command updates documentation for "My Product". This will perform a `git pull` on the `master` branch and publish any missing tags.

You may use the `docweaver:update-all` artisan command to update documentation for all products.