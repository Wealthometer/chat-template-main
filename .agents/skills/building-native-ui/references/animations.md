# Animations

Use Reanimated v4. Avoid React Native's built-in Animated API.

## Entering and Exiting Animations

Use Animated.View with entering and exiting animations. Layout animations can animate state changes.

```tsx
import Animated, {
  FadeIn,
  FadeOut,
  LinearTransition,
} from "react-native-reanimated";

function App() {
  return (
    <Animated.View
      entering={FadeIn}
      exiting={FadeOut}
      layout={LinearTransition}
    />
  );
}
```

## On-Scroll Animations

Create high-performance scroll animations using Reanimated's hooks:

```tsx
import Animated, {
  useAnimatedRef,
  useScrollViewOffset,
  useAnimatedStyle,
  interpolate,
} from "react-native-reanimated";
