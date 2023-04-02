# Send Push Notification Package

This package provides a simple way to send notifications using the [Pushover](https://pushover.net/) service. It exports a single function, `sendPushOverNotification`, which you can use to send a notification with a given payload.

## Installation

To install the package, use your favorite package manager:

```bash
npm install --save send-push-notification
```

or

```bash
yarn add send-push-notification
```

## Usage

First, you need to set your Pushover user key and API token as environment variables:

```bash
export PUSHOVER_USER_KEY=your_user_key
export PUSHOVER_API_TOKEN=your_api_token
```

Then, you can use the `sendPushOverNotification` function to send a notification:

```javascript
import { sendPushOverNotification } from 'send-push-notification';

const payload = {
    message: 'Hello, World!',
    title: 'My First Notification',
    // Other optional parameters: https://pushover.net/api#messages
};

sendPushOverNotification(payload)
    .then(response => {
        console.log('Notification sent successfully:', response);
    })
    .catch(error => {
        console.error('Failed to send notification:', error);
    });
```

## Error Handling

In case of an error, the function will throw an error with a descriptive message. You can handle the error using a try-catch block or with a `.catch()` method in a promise chain.

## API Reference

For more information about the Pushover API and the available parameters, please refer to the official [Pushover API documentation](https://pushover.net/api).

## License

This package is licensed under the MIT License.
