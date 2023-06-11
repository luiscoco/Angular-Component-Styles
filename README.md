# component-styles

In Angular, component styles refer to the way you define and apply styles to individual components. Angular provides several options for defining component styles, allowing you to encapsulate the styles within the component and avoid global style conflicts.

There are three main approaches to defining component styles in Angular:

## Inline Styles: 
You can define styles directly in the component's template using the style attribute. For example:

```typescript
@Component({
  selector: 'app-sample',
  template: `
    <div style="color: blue; font-size: 16px;">
      This is a sample component with inline styles.
    </div>
  `,
})
export class SampleComponent {
  // Component logic goes here
}
```

## External Stylesheet:
You can define styles in an external CSS file and link it to the component using the styleUrls property. For example:

```typescript
<!-- sample.component.html -->
<div class="sample-component">
  This is a sample component with external styles.
</div>

/* sample.component.css */
.sample-component {
  color: red;
  font-size: 18px;
}

@Component({
  selector: 'app-sample',
  templateUrl: 'sample.component.html',
  styleUrls: ['sample.component.css']
})
export class SampleComponent {
  // Component logic goes here
}
```

## Component-specific styles: 
You can define styles directly in the component's TypeScript file using the styles property. This approach allows you to define styles specific to a component without using an external file. For example:

```typescript
@Component({
  selector: 'app-sample',
  template: `
    <div class="sample-component">
      This is a sample component with component-specific styles.
    </div>
  `,
  styles: [`
    .sample-component {
      color: green;
      font-size: 20px;
    }
  `]
})
export class SampleComponent {
  // Component logic goes here
}
```

With these approaches, you can apply styles to individual Angular components based on your preference and project requirements.

