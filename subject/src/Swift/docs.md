# SwiftUI Components and Concepts

This guide covers the main SwiftUI components and concepts we'll use in this project.

## Core Components

### Views and Navigation

-   **NavigationView**: Creates a navigation hierarchy for your app
    -   [Documentation](https://developer.apple.com/documentation/swiftui/navigationview)
-   **TabView**: Creates a view that switches between multiple child views
    -   [Documentation](https://developer.apple.com/documentation/swiftui/tabview)

### Input Components

-   **TextField**: Captures text input from users
    -   [Documentation](https://developer.apple.com/documentation/swiftui/textfield)
-   **Toggle**: Creates a checkbox or switch control
    -   [Documentation](https://developer.apple.com/documentation/swiftui/toggle)
-   **Button**: Creates a tappable button with custom actions
    -   [Documentation](https://developer.apple.com/documentation/swiftui/button)

### Display Components

-   **Text**: Displays one or more lines of read-only text
    -   [Documentation](https://developer.apple.com/documentation/swiftui/text)
-   **List**: Creates a scrolling table of data
    -   [Documentation](https://developer.apple.com/documentation/swiftui/list)

### API Call Example

```swift
// Model
struct Todo: Codable {
    let id: Int
    let title: String
    let completed: Bool
}

// API Service
class APIService {
    func fetchTodos() async throws -> [Todo] {
        guard let url = URL(string: "https://api.example.com/todos") else {
            throw URLError(.badURL)
        }

        let (data, _) = try await URLSession.shared.data(from: url)
        return try JSONDecoder().decode([Todo].self, from: data)
    }
}

// Usage in View
struct ContentView: View {
    @State private var todos: [Todo] = []
    @State private var errorMessage: String?

    var body: some View {
        List(todos, id: \.id) { todo in
            Text(todo.title)
        }
        .task {
            do {
                todos = try await APIService().fetchTodos()
            } catch {
                errorMessage = error.localizedDescription
            }
        }
    }
}
```

## Automatic Dark Mode and Light Mode

SwiftUI provides built-in support for dark and light modes. Your app will automatically adapt to the user's system settings.

```swift
// Example of custom colors that adapt to color scheme
Color("AccentColor") // Define in Assets.xcassets with dark/light variants

// Force a specific color scheme
.preferredColorScheme(.dark) // or .light
````

Learn more about [Dark Mode](https://developer.apple.com/documentation/swiftui/supporting-dark-mode-in-your-interface)

## Responsive Design

SwiftUI uses a declarative approach to handle different screen sizes and orientations:

### Dynamic Type

```swift
Text("Hello")
    .font(.body) // Automatically adapts to user's preferred text size
```

### Adaptive Layout

```swift
// Example of adaptive layout
HStack {
    if horizontalSizeClass == .compact {
        // Phone layout
    } else {
        // iPad/landscape layout
    }
}
```

### GeometryReader

```swift
GeometryReader { geometry in
    // Use geometry.size to create responsive layouts
}
```

Learn more about [Layout and Views](https://developer.apple.com/documentation/swiftui/view-layout-and-presentation)

## Additional Resources

-   [SwiftUI Documentation](https://developer.apple.com/documentation/swiftui)
-   [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines)
-   [SwiftUI Tutorials](https://developer.apple.com/tutorials/swiftui)
-   [Apple Developer Forums](https://developer.apple.com/forums/tags/swiftui)

**Note:** SwiftUI is constantly evolving. Always refer to the latest Apple documentation for the most up-to-date information.
