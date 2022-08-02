## Laravel Docker 

This is a Laravel Docker boilerplate repo

### Services List

- **[NGINX](https://hub.docker.com/_/nginx)**
- **[MYSQL - mariadb](https://hub.docker.com/_/mariadb)**
- **[PHP8.1](https://hub.docker.com/_/php)**
- **[COMPOSER](https://hub.docker.com/_/composer)**
- **[NODE - node:current-alpine](https://hub.docker.com/_/composer)**





## Setup Instructions (Linux/Ubuntu)

1. Clone the project from the repository to your local machine.

2. Open the project in your preferred code editor or IDE with a terminal and continue the below steps.
   
3. Changes the ports in the `docker-compose.yml` and `nginx/default.conf` file if needed. 

4. Create 2 folders `mysql` and `src` after cloning the project.

Test : Create a `src/public` folder and add a `index.php` file to test if it is indexing the correct file.  

5. Docker build

   ``` 
   sudo docker-compose up -d --build 
   ```
-d flag used to run docker in the background.

6. Create Laravel project 

    ``` 
    sudo docker-compose run --rm composer create-project --prefer-dist laravel/laravel . 
    ```

This will create a Laravel 9 project inside src directory. Specify the Laravel version if needed.

7. Install composer packages 

    ``` 
    sudo docker-compose run --rm composer create require YOUR_PACKAGE 
    ```

8. Install npm 

    ``` 
    sudo docker-compose run --rm npm install 
    ```

9. Run artisan commands 

    ``` 
    sudo docker-compose run --rm artisan YOUR_COMMAND 
    ```

10. Bring down Docker 

    ``` 
    sudo docker-compose down
    ```

11. Show Docker service list

    ``` 
    sudo docker-compose ps 
    ```

#### Other

If you face any error related to permission denied, check if the folders/files are locked. Run this command on your linux to unlock all the files and folders. 

    ``` 
    sudo chmod o+w FOLDER/* -R
    ```

## ENJOY! 
