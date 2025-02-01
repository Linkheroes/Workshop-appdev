# Ionic Angular Components and Concepts

This guide covers the main Ionic components and concepts we'll use in this project with Angular integration.

## Core Components

### Navigation

-   **Ion-Tabs**: Creates a tabbed interface for navigation
    -   [Documentation](https://ionicframework.com/docs/api/tabs)
-   **Ion-Nav**: Provides stack-based navigation
    -   [Documentation](https://ionicframework.com/docs/api/nav)

### Input Components

-   **Ion-Input**: Creates text input fields
    -   [Documentation](https://ionicframework.com/docs/api/input)
-   **Ion-Checkbox**: Creates a checkbox control
    -   [Documentation](https://ionicframework.com/docs/api/checkbox)
-   **Ion-Button**: Creates styled buttons
    -   [Documentation](https://ionicframework.com/docs/api/button)

### Display Components

-   **Ion-Text**: Displays styled text
    -   [Documentation](https://ionicframework.com/docs/api/text)
-   **Ion-List**: Creates lists of items
    -   [Documentation](https://ionicframework.com/docs/api/list)
-   **Ion-Card**: Creates card containers
    -   [Documentation](https://ionicframework.com/docs/api/card)

## Usage Examples

### Basic Page Structure

```typescript
@Component({
  selector: 'app-home',
  template: `
    <ion-header>
      <ion-toolbar>
        <ion-title>Home</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content>
      <!-- Page content here -->
    </ion-content>
  `
})
```

### Form Elements

```typescript
<ion-list>
  <ion-item>
    <ion-label position="floating">Username</ion-label>
    <ion-input [(ngModel)]="username"></ion-input>
  </ion-item>

  <ion-item>
    <ion-label>Remember me</ion-label>
    <ion-checkbox [(ngModel)]="remember"></ion-checkbox>
  </ion-item>
</ion-list>
```

### API Call Example

```typescript
// In your service
@Injectable({
    providedIn: "root",
})
export class ApiService {
    constructor(private http: HttpClient) {}

    getTodos(): Observable<Todo[]> {
        return this.http.get<Todo[]>("https://api.example.com/todos");
    }
}

// In your component
export class TodoListComponent {
    todos: Todo[] = [];

    constructor(private apiService: ApiService) {
        this.apiService.getTodos().subscribe(
            (data) => (this.todos = data),
            (error) => console.error("Error fetching todos:", error)
        );
    }
}
```

## Dark Mode and Theming

Ionic provides built-in support for dark mode:

```typescript
// In your component
const toggleDarkMode = () => {
    document.body.classList.toggle("dark");
};
```

```css
/* In your variables.scss */
:root {
    --ion-color-primary: #428cff;
}

.dark {
    --ion-color-primary: #54a0ff;
}
```

## Responsive Design

Ionic handles responsive design automatically with CSS Grid and Flexbox:

```typescript
<ion-grid>
  <ion-row>
    <ion-col size="12" size-md="6">
      <!-- Content adapts to screen size -->
    </ion-col>
  </ion-row>
</ion-grid>
```

## Additional Resources

-   [Ionic Documentation](https://ionicframework.com/docs)
-   [Angular Integration](https://ionicframework.com/docs/angular/overview)
-   [Ionic Components](https://ionicframework.com/docs/components)
-   [Theming Guide](https://ionicframework.com/docs/theming/basics)

**Note:** Always check the official Ionic documentation for the most up-to-date information and best practices.
