# React Native Legacy Custom Components

This is a module for legacy "CustomComponents" to gracefully deprecate.

## Navigator

The navigator component in this module will behave identically as the one in old version of React native, with one exception:

Latest documentation is available here: http://facebook.github.io/react-native/releases/0.43/docs/navigator.html


### Breaking Changes from react-native

- Navigator.props.sceneStyle must be a plain object, not a stylesheet!

(this breaking change is needed to avoid calling React Native's private APIs)


# 本插件修改过两个地方
屏蔽了isMounted,在0.44以上会报警告

    _handleSpringUpdate: function() {
    // if (!this.isMounted()) {
    //   return;
    // }
    // Prioritize handling transition in progress over a gesture:

    _completeTransition: function() {
    // if (!this.isMounted()) {
    //   return;
    // }
