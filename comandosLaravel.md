php artisan migrate:update = HACES LAS MIGRACIONES ACTUALIZADAS
php artisan migrate:rollback = HACES ROLLBACK A LAS MIGRACIONES
php artisan serve = CORRER EL PROYECTO

 # Flujo nueva integración de una tabla nueva y su CRUD 
php artisan make:migration empleados
php artisan migrate:fresh --seed
php artisan make:crud empleados

 # para que jale 
composer require laravel/ui
php artisan ui bootstrap --auth
npm install
npm run dev
composer require ibex/crud-generator --dev
publish --tag=laravel-assets --ansi
php artisan vendor:publish --tag=crud
php artisan make:crud "nombre de tabla"

# alert Swal
npm install sweetalert2
npm run dev

# Si se modificia el archivo app.php para ver reflejados los cambios se usa 
php artisan config:clear

# instalar y usar icon packages
composer require codeat3/blade-carbon-icons
página: https://blade-ui-kit.com/blade-icons
ejemplo:
```html
<x-carbon-apple style="color: green"/>
```

# Para hacer link simbolico de la carpeta storage/public  y acceder desde su URL
php artisan storage:link

# Para que funcione correctamente el gitignore
 git rm -r --cached .
 git commit -m "fixed untracked files"
 git push ó subirlo mediente desktop

# Para crear un seeder ejemplo de rol
php artisan make:seeder RoleSeeder 

# Para que funcione el seeder (se llenan las tablas solas)
php artisan migrate:fresh --seed

# Para llenar tablas en  producción OJO SOBREESCRIBE TODO
migrate:fresh --seed --force

# Comandos para realizar CRON
php artisan make:command DeleteFileTask
php artisan schedule:list
php artisan schedule:run
php artisan schedule:test

# Comandos de Permisos
composer require spatie/laravel-permission
php artisan vendor:publish --provider="Spatie\Permission\PermissionServiceProvider"
php artisan migrate:fresh --seed
Se añade al modelo user.php la linea use Spatie\Permission\Traits\HasRoles;