# 🧩 CSock

**CSock** is a minimal and elegant C# socket library that simplifies networking in your applications. Built for clarity and flexibility, CSock allows you to quickly integrate TCP socket functionality with minimal boilerplate.

---

## ✨ Features

- ⚡ Easy TCP socket creation and cleanup
- 📥 Reliable data sending & receiving
- 🧠 Intelligent socket state detection
- ⏱ Configurable send/receive timeouts
- 🔌 Lightweight and dependency-free

---

## 📦 Installation

**Coming soon to NuGet!**  
For now, clone and add the source manually:


Include the `CSock` namespace in your project:

```csharp
using CSock;
```

---

## 🧪 Quick Start

```csharp
using System;
using System.Net;
using System.Net.Sockets;
using CSock;

class Program
{
    static void Main()
    {
        var socket = Sockets.CreateSocket();
        var endpoint = new IPEndPoint(IPAddress.Loopback, 12345);

        Sockets.BindSocketToEndpoint(socket, endpoint);

        byte[] data = System.Text.Encoding.UTF8.GetBytes("Hello, CSock!");
        Sockets.SendDataToSocket(socket, data, data.Length);

        Sockets.ShutdownSocket(socket);
        Sockets.CloseSocket(socket);
    }
}
```

---

## 🧰 API Overview

| Method                          | Description                                      |
|-------------------------------|--------------------------------------------------|
| `CreateSocket()`              | Creates a new TCP socket                        |
| `BindSocketToEndpoint()`      | Binds the socket to a local IP and port         |
| `SendDataToSocket()`          | Sends a byte buffer to the connected endpoint   |
| `ReceiveDataFromSocket()`     | Receives incoming data                          |
| `ShutdownSocket()`            | Gracefully shuts down both send and receive     |
| `CloseSocket()`               | Closes and releases the socket                  |
| `CleanSocket()`               | Disposes the socket resources                   |
| `IsSocketConnected()`         | Checks if the socket is still connected         |
| `SetSocketTimeout()`          | Configures socket timeouts                      |

---

## 🔮 Planned Features

- ✅ UDP support  
- ✅ Asynchronous socket wrappers  
- ✅ Server-side helpers  
- ✅ Built-in diagnostics

---

## 📝 License

**MIT License**  
© 2025 [Your Name]

---

## 🤝 Contributing

Pull requests, issues, and ideas are always welcome!  
Let's build simple networking tools together.
