https://www.youtube.com/watch?v=y7U0q7p2_4w

# sail artisan make:observer TravelObserver --model=Travel

# Slug
https://github.com/cviebrock/eloquent-sluggable

# tinker
App\Models\Travel::create(['name' => 'Some thing', 'description' => 'aaa', 'number_of_days' => 5]);

# tests
sail artisan make:test TravelsListTest
sail artisan make:test LoginTest

sail artisan test --filter=ToursListTest

# alias 
alias sail='[ -f sail ] && sh sail || sh vendor/bin/sail'

# filtering 
http://localhost/api/v1/travels/some-thing/tours?priceFrom=80&dateFrom=2023-12-15&sortBy=price&sortOrder=asc


# deploy
docker run --rm \
-u "$(id -u):$(id -g)" \
-v "$(pwd):/var/www/html" \
-w /var/www/html \
laravelsail/php82-composer:latest \
composer install --ignore-platform-reqs

# create command
sail artisan make:command CreateUserCommand

# create user
sail artisan users:create

# create seeder
sail artisan make:seeder RoleSeeder

# run seeder
sail artisan db:seed --class=RoleSeeder

# create invokable controller
sail artisan make:controller Api/V1/Auth/LoginController --invokable
