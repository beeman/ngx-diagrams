# ngx-diagrams (WIP)
___

[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)
[![Build Status](https://travis-ci.com/DanielNetzer/ngx-diagrams.svg?branch=master)](https://travis-ci.com/DanielNetzer/ngx-diagrams)

***Light weight, modular, typed diagram engine for angular.***

Check out our [stories](https://danielnetzer.github.io/ngx-diagrams)

# Getting Started
___

### Installation

```bash
npm i ngx-diagrams
```

### Setup
- Import the library module.
  
`app.module.ts`

```javascript
import { NgxDiagramsModule } from 'ngx-diagrams';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    NgxDiagramsModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

- instantiate new DiagramModel in the component you want to add the diagram canvas (e.g. app.component.ts), and start adding nodes, links, ports and work with the diagram.
  
    `app.component.ts`

```javascript
 diagramModel = new DiagramModel();

  constructor() { }

  ngOnInit() {
    const newNode = this.diagramModel.addNode('test', 200, 300);
    newNode.addPort('test', 'out');
  }
```