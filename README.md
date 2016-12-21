# Angular 2 Component LifeCycle
List of lifecycle hooks.

    
    @Component({
      selector: 'some-selector',
      template: '<h1>Some title</h1>',
    })
    
    // Component controller
    export class MyComponent {
    
      ngOnInit() {
        // Properties are resolved and things like
        // this.mapWindow and this.mapControls
        // had a chance to resolve from the
        // two child components <map-window> and <map-controls>
      }
      
      ngOnDestroy() {
        // Speak now or forever hold your peace
      }
      
      ngDoCheck() {
        // Custom change detection
      }
      
      ngOnChanges(changes) {
        // Called right after our bindings have been checked but only
        // if one of our bindings has changed.
        //
        // changes is an object of the format:
        // {
        //   'prop': PropertyUpdate
        // }
      }
      
      ngAfterContentInit() {
        // Component content has been initialized
      }
      
      ngAfterContentChecked() {
        // Component content has been Checked
      }
      
      ngAfterViewInit() {
        // Component views are initialized
      }
      
      ngAfterViewChecked() {
        // Component views have been checked
      }
      
    }
