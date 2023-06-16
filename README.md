# sail artisan make:observer TravelObserver --model=Travel

# Slug
https://github.com/cviebrock/eloquent-sluggable

# tinker
App\Models\Travel::create(['name' => 'Some thing', 'description' => 'aaa', 'number_of_days' => 5]);

# tests
sail artisan make:test TravelsListTest
sail artisan test --filter=ToursListTest


http://localhost/api/v1/travels/some-thing/tours?priceFrom=80&dateFrom=2023-12-15&sortBy=price&sortOrder=asc

