Status: done

fixear todos los warining que se producne cuando levantas el server de la UI

## Implementation Notes

Implemented and pushed to the following branches:
- `consorcio-unido-ui`: `fix-ui-warning`

All ESLint warnings emitted by `npm start` were fixed (unused vars/imports, async `useEffect` callbacks, missing hook dependencies, anonymous default export). Remaining `fs.F_OK` and `onAfterSetupMiddleware`/`onBeforeSetupMiddleware` deprecation warnings originate from `react-scripts 5.0.1`'s internal webpack-dev-server config, not application code, and are out of scope without ejecting/overriding the CRA webpack config.
