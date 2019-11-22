laravel new serverPHP
cd serverPHP
php artisan serve
copy .env.example .env
php artisan key:generate
#criar banco de dados e setar em .env
#em app/AppServiceProvider.php adicionar:
use Illuminate\Support\Facades\Schema;
#dentro do método boot escrever:
Schema::defaultStringLength(191);
php artisan make:migrate
php artisan make:migration create_tasks_table
#adicione as colunas necessárias e depois execute 
php artisan migrate
#crie o model e o controller
php artisan make:model Task
php artisan make:controller TaskController
#va no model criado e preencha com extends model
#preencha com os campos necessarios pesquisar por model fillable
#no controller crie os métodos na mao