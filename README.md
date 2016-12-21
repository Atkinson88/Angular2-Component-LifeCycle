# Angular 2 Component LifeCycle
List of lifecycle hooks.

    
    @Component({
      selector: 'some-selector',
      template: '<h1>Some title</h1>',
    })
    
    // Component controller
    export class MyComponent {
    
      constructor(){}
    
      ngOnInit() {
        // Initialize the directive/component after Angular initializes the data-bound input properties.
      }
      
      ngOnDestroy() {
        // Just before Angular destroys the directive/component.
      }
      
      ngDoCheck() {
        // Detect and act upon changes that Angular can or won’t detect on its own. Called every change detection run.
      }
      
      ngOnChanges(changes) {
        
        // Respond after Angular sets a data-bound input property. The method receives a changes object of current and previous values.
        
        // changes is an object of the format:
        // {
        //   'prop': PropertyUpdate
        // }
      }
      
      ngAfterContentInit() {
        // After Angular projects external content into its view.
      }
      
      ngAfterContentChecked() {
        // 	After Angular checks the bindings of the external content that it projected into its view.
      }
      
      ngAfterViewInit() {
        // After Angular creates the component’s view(s).
      }
      
      ngAfterViewChecked() {
        // 	After Angular checks the bindings of the component’s view(s).
      }
      
    }
