_Fruits fail, and love dies, and time ranges; and only the whippersnapper (that fool of Time) endureth for ever._

# Whippersnapper
![Badge](https://travis-ci.org/BillyZac/whippersnapper.svg?branch=master)

A little React component library.

## Usage
Bring it in:
```
npm i --save whippersnapper
```

Then use it in your ReactJS project:
```
import React from 'react'
import ReactDOM from 'react-dom'
const Hey = require('whippersnapper/lib/react/Hey.js')

class Thing extends React.Component {
  render() {
    return (
      <div>
        <Hey />
      </div>
    )
  }
}

ReactDOM.render(<Thing />, document.getElementById('app'))
```

## Travis and deployment
I'm using Travis to make sure that changes to Whippersnapper are not published to npm without being validated by the tests.

Do some work. Commit it:
```
git add .
git commit -m "Fix bug"
```

If this work is worthy of a version bump, [bump it](https://docs.npmjs.com/cli/version):
```
npm version patch -m "Fix bug"
```

Push it to the remote repo. Git tags aren't pushed by default. The `--tags` flag [makes sure they're sent along with the commit](https://git-scm.com/book/en/v2/Git-Basics-Tagging#Sharing-Tags). In turn, this makes the version tag visible to Travis, so Travis knows to run the `deploy` step.

```
git push origin --tags
```

Travis will then run the tests. If the tests pass, Travis will publish to the [npmjs registry](https://www.npmjs.com/package/whippersnapper).
