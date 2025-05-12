# Build an AI Agent from Scratch with Rasa
This is a demo AI Agent prepared for an online live session - Learn Live: Build an AI Agent from Scratch with Rasa, [link](https://www.meetup.com/rasahq/events/307564079/?utm_medium=referral&utm_campaign=share-btn_savedevents_share_modal&utm_source=link)

### Steps

1. **Create a Codespace:**
   - Click on the green "Code" button on this page, then scroll down to "Codespaces".
   - Click on "Create codespace on main".

2. **Set Up Environment:**
   - In the codespace, create the `.env` file, add your [Rasa license key](https://rasa.com/rasa-pro-developer-edition-license-key-request/) and OpenAI API key to that file (see `.env.example` file)
     ```
     RASA_PRO_LICENSE='your_rasa_pro_license_key_here'
     OPENAI_API_KEY='your_openai_api_key_here'
     ```
   - Set this environment variables by running 
     ```
     source .env
     ```
   - Activate your python environment by running
     ```
     source .venv/bin/activate
     ```

3. **Train the Model:**
   - In the terminal, run:
     ```
     rasa train
     ```

4. **Talk to your Bot:**
   - In the terminal, run
     ```
     rasa inspect
     ```
     GitHub will show a notification, click on the green button to view the inspector where you can chat with your assistant.

5. **Run Custom Actions:**
  In Rasa 3.10 and later, custom actions are automatically run as part of your running assistant. To double-check that this is set up correctly, ensure that your `endpoints.yml` file contains the following configuration:
   ```
   action_endpoint:
      actions_module: "actions" # path to your actions package
    ```
   Then re-run your assistant via `rasa inspect` every time you make changes to your custom actions.