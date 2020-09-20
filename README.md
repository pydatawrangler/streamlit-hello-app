# streamlit-hello-app
Our very first streamlit app deployed on heroku

## Instructions
1. Create a repository on github and clone in your PC
2. Navigate to that folder in the terminal
3. Make a file named app.py
4. Make a file named Procfile and paste this

	```
    web: sh setup.sh && streamlit run app.py
    ```

5. Make a file named requirements.txt
6. Make a file named setup.sh and paste this
	
    ```
    mkdir -p ~/.streamlit/

    echo "\
    [server]\n\
    headless = true\n\
    port = $PORT\n\
    enableCORS = false\n\
    \n\
    " > ~/.streamlit/config.toml
    ```

7. Create app in Heroku
    ```
    heroku login
    heroku create *name-of-app*
    ```
8. Git commit
    ```
    git add .
    git commit -m "Some message"
    ```
9. Push to heroku
    ```
    git push heroku master
    ```