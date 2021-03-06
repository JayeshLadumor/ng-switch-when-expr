# ng-switch-when-expr

Improves `ng-switch-when` to handle expressions instead of magic values. Useful for dealing with constants and enums.

```html
<div ng-switch on="myCtrk.dayOfWeek">
    <span ng-switch-when-expr="myCtrl.days.SUNDAY">Sunday morning</span>
    <span ng-switch-when-expr="myCtrl.days.MONDAY"><b>Monday evening</b></span>
    <span ng-switch-when-expr="myCtrl.days.SATURDAY"><i>Saturday afternoon</i></span>
    <div ng-switch-when-expr="'THURSDAY'">
        <ul>
            <li>On Thursday</li>
            <li>Only on Thursday</li>
        </ul>
    </div>
    <span ng-switch-default>Some day...</span>
</div>
```

## Installation

1. Run `bower install ngswitchwhenexpr`

2. Import the script in your `index.html` after `angular.js`

3. Add the module `mallowigi.ngUtils` to your main module.

`angular.module('mainModule', ['mallowigi.ngUtils']);`

4. Use it instead of `ng-switch-when` when you want to use expressions.
