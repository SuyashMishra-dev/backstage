## API Report File for "@backstage/config-loader"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { AppConfig } from '@backstage/config';
import { JsonObject } from '@backstage/config';
import { JSONSchema7 } from 'json-schema';

// @public
export type ConfigSchema = {
  process(
    appConfigs: AppConfig[],
    options?: ConfigProcessingOptions,
  ): AppConfig[];
  serialize(): JsonObject;
};

// @public
export type ConfigVisibility = typeof CONFIG_VISIBILITIES[number];

// @public (undocumented)
export function loadConfig(options: LoadConfigOptions): Promise<AppConfig[]>;

// @public (undocumented)
export type LoadConfigOptions = {
  configRoot: string;
  configPaths: string[];
  env?: string;
  experimentalEnvFunc?: EnvFunc;
};

// @public
export function loadConfigSchema(options: Options): Promise<ConfigSchema>;

// @public
export function mergeConfigSchemas(schemas: JSONSchema7[]): JSONSchema7;

// @public
export function readEnvConfig(env: {
  [name: string]: string | undefined;
}): AppConfig[];

// (No @packageDocumentation comment for this package)
```
