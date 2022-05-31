react-custom-scrollbars-extended
=========================
## Quick note
This repo is due to the original (fantastic) [`react-custom-scrollbars`](https://www.npmjs.com/package/react-custom-scrollbars) package going a little stale and we needed a handful of bug fixes which will be managed here.

## Installation
```bash
npm install react-custom-scrollbars-extended --save
```

This assumes that you’re using [npm](http://npmjs.com/) package manager with a module bundler like [Webpack](http://webpack.github.io) or [Browserify](http://browserify.org/) to consume [CommonJS modules](http://webpack.github.io/docs/commonjs.html).

## Usage

This is the minimal configuration. [Check out the Documentation for advanced usage](https://github.com/aataa-fa/react-scrollbars/tree/master/docs).

```javascript
import { Scrollbars } from 'react-custom-scrollbars-extended';

class App extends Component {
  render() {
    return (
      <Scrollbars style={{ width: 500, height: 300 }}>
        <p>Some great content...</p>
      </Scrollbars>
    );
  }
}
```

The `<Scrollbars>` component is completely customizable. Check out the following code:

```javascript
import { Scrollbars } from 'react-custom-scrollbars-extended';

class CustomScrollbars extends Component {
  render() {
    return (
      <Scrollbars
        onScroll={this.handleScroll}
        onScrollFrame={this.handleScrollFrame}
        onScrollStart={this.handleScrollStart}
        onScrollStop={this.handleScrollStop}
        onUpdate={this.handleUpdate}
        renderView={this.renderView}
        renderTrackHorizontal={this.renderTrackHorizontal}
        renderTrackVertical={this.renderTrackVertical}
        renderThumbHorizontal={this.renderThumbHorizontal}
        renderThumbVertical={this.renderThumbVertical}
        autoHide
        autoHideTimeout={1000}
        autoHideDuration={200}
        autoHeight
        autoHeightMin={0}
        autoHeightMax={200}
        thumbMinSize={30}
        universal={true}
        {...this.props}>
    );
  }
}
```

## License

MIT
