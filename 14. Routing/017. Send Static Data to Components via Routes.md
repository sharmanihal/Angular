
### Static Data with the `data` Property
The `data` property in the Angular router configuration allows you to define static data that is passed to the component whenever a route is loaded. This data remains the same each time you navigate to that route.

#### Example:
In your route configuration, you might set up something like:
```typescript
const routes: Routes = [
  {
    path: 'users/:userId',
    component: UserTasksComponent,
    data: { message: 'Hello!' }  // Static data
  }
];
```
Here, `message` is static data that doesn’t change, and it’s defined once in the route configuration.

In the `UserTasksComponent`, with `componentInputBinding` enabled, you can receive this `message` as an input:
```typescript
@Component({
  selector: 'app-user-tasks',
  template: `<p>{{ message }}</p>`
})
export class UserTasksComponent {
  message=input.required<string>()  // Automatically gets the 'Hello!' message from the route data
}
```

But to access this data , we need to make sure we have addded withComponentInputBinding() to our config:

![image](https://github.com/user-attachments/assets/b7bb670f-ea81-4888-86e3-106cd97f4622)

