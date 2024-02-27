
//add this in pagination.css
/* resources/css/pagination.css */

.pagination {
    display: flex;
    justify-content: center;
    align-items: center;
    list-style: none;
}

.pagination-item {
    margin: 0 4px;
}

.pagination-link {
    display: inline-block;
    padding: 8px 16px;
    border: 1px solid #4299e1;
    border-radius: 4px;
    color: #4299e1;
    text-decoration: none;
    transition: background-color 0.3s, color 0.3s;
}

.pagination-link:hover {
    background-color: #4299e1;
    color: white;
}

.pagination-link.active {
    background-color: #4299e1;
    color: white;
}



//add this on the mixpack.mix.js
const mix = require('laravel-mix');

mix.js('resources/js/app.js', 'public/js')
   .postCss('resources/css/app.css', 'public/css', [
        require('tailwindcss'),
        // Other postcss plugins if needed
    ])
   .postCss('resources/css/pagination.css', 'public/css');


//run this
npm run dev

   
