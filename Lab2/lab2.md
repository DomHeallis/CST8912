flowchart TD
    %% Firewall and Load Balancer
    A([Firewall]) --> B([Load Balancer])

    %% Left Side
    B --> C["User Browser\nReact"]
    C --> D["Web Server (Flask)\nVirtual Machine 1"]
    D --> F["Database (Postgre)\nVirtual Machine"]

    %% Right Side
    B --> E["User Browser\nReact"]
    E --> G["Web Server (Flask)\nVirtual Machine 2"]
    G --> F

    %% Second Database connected
    F --> H["Database (Postgre)\nVirtual Machine"]