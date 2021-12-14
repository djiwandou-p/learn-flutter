# launch.json
```json
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "[Stag] Evermos",
            "request": "launch",
            "type": "dart",
            "program": "lib/main.dart",
            "args": [
                "--flavor",
                "staging",
                "--dart-define",
                "FLAVOR_TYPE=staging",
                "--dart-define",
                "BASIC_AUTHORIZATION=Y2xpZW50X2FuZHJvaWQ6M3Yzcm0wcw==",
                "--dart-define",
                "AVO_API_KEY=iQ3ReDCfc1vVZrxC74aa",
                "--dart-define",
                "AMPLITUDE_API_KEY=28e8b7a07c70beef6134911d1fa3de0f",
                "--dart-define",
                "RUDDERSTACK_WRITE_KEY=1uNTjxaFaEHx7ETEquCQPeYfqok",
            ]
        },
        {
            "name": "[Prev] Evermos",
            "request": "launch",
            "type": "dart",
            "program": "lib/main.dart",
            "args": [
                "--flavor",
                "preview",
                "--dart-define",
                "FLAVOR_TYPE=preview",
                "--dart-define",
                "BASIC_AUTHORIZATION=Y2xpZW50X2FuZHJvaWQ6M3Yzcm0wcw==",
                "--dart-define",
                "AVO_API_KEY=iQ3ReDCfc1vVZrxC74aa",
                "--dart-define",
                "AMPLITUDE_API_KEY=28e8b7a07c70beef6134911d1fa3de0f",
                "--dart-define",
                "RUDDERSTACK_WRITE_KEY=20z57MMlEEiwnslYvbVBteKQ7Al",
            ]
        },
        {
            "name": "[Prod] Evermos",
            "request": "launch",
            "type": "dart",
            "program": "lib/main.dart",
            "args": [
                "--flavor",
                "production",
                "--release",
                "--dart-define",
                "FLAVOR_TYPE=production",
                "--dart-define",
                "BASIC_AUTHORIZATION=Y2xpZW50X2FuZHJvaWQ6M3Yzcm0wcw==",
                "--dart-define",
                "AVO_API_KEY=iQ3ReDCfc1vVZrxC74aa",
                "--dart-define",
                "AMPLITUDE_API_KEY=28e8b7a07c70beef6134911d1fa3de0f",
                "--dart-define",
                "RUDDERSTACK_WRITE_KEY=20z57MMlEEiwnslYvbVBteKQ7Al",
            ]
        }
    ]
}
```