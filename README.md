# How to Set Up 💻

## 1. Prepare a Rocket.Chat Server

Ensure you have a Rocket.Chat server ready. If you don't have one, follow this [guide](https://developer.rocket.chat/v1/docs/server-environment-setup).

## 2. Install the Rocket.Chat Apps Engine CLI

Install the CLI globally using npm:

```sh
npm install -g @rocket.chat/apps-cli
```

Verify if the CLI has been installed:

```sh
rc-apps -v
# Example output: @rocket.chat/apps-cli/1.4.0 darwin-x64 node-v10.15.3
```

## 3. Clone the GitHub Repository

```sh
git clone https://github.com/ishanmitra/troubleshoot-rocketchat-extendcommand.git
```

## 4. Navigate to the Repository

```sh
cd troubleshoot-rocketchat-extendcommand
```

## 5. Install App Dependencies

```sh
npm install
```

## 6. Enable Apps Development Mode

To install private Rocket.Chat Apps, the server must be in development mode. Enable it by navigating to:

**Administration > General > Apps** and turn on **"Enable development mode"**.

## 7. Deploy the App to the Server

```sh
rc-apps deploy --url <server_url> --username <username> --password <password>
```

- If running the server locally, `server_url` is [http://localhost:3000](http://localhost:3000). If using another port, replace `3000` with the correct port.
- `<username>` is the admin username.
- `<password>` is the admin password.

## Expected Behaviour

After the app has been deployed, execute the slash command `/extend-message` in any channel.

When you execute the registered slash command, a message is sent to the current channel and altered to include an image attachment and a custom field. The attached image is visible in the message after editing. In addition, the created custom fields are accessible from any database client of your choosing.

### Current Issue:

**rocket.cat** shows the following error message:  
Something went wrong while executing command: `/extend-message` 
