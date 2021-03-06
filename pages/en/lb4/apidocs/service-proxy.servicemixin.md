---
lang: en
title: 'API docs: service-proxy.servicemixin'
keywords: LoopBack 4.0, LoopBack 4
sidebar: lb4_sidebar
editurl: https://github.com/strongloop/loopback-next/tree/master/packages/service-proxy
permalink: /doc/en/lb4/apidocs.service-proxy.servicemixin.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/service-proxy](./service-proxy.md) &gt; [ServiceMixin](./service-proxy.servicemixin.md)

## ServiceMixin() function

A mixin class for Application that creates a .serviceProvider() function to register a service automatically. Also overrides component function to allow it to register repositories automatically.

<b>Signature:</b>

```typescript
export declare function ServiceMixin<T extends MixinTarget<Application>>(superClass: T): {
    new (...args: any[]): {
        serviceProvider<S>(provider: Constructor<Provider<S>>, nameOrOptions?: string | ServiceOptions | undefined): Binding<S>;
        component<T_1 extends Component = Component>(componentCtor: Constructor<T_1>, nameOrOptions?: string | BindingFromClassOptions | undefined): Binding<T_1>;
        mountComponentServices<T_2 extends Component = Component>(component: Constructor<T_2>, componentBindingKey?: string | BindingKey<T_2> | undefined): void;
        readonly options: ApplicationConfig;
        readonly state: string;
        controller: <T_3>(controllerCtor: Constructor<T_3>, nameOrOptions?: string | BindingFromClassOptions | undefined) => Binding<T_3>;
        server: <T_4 extends Server>(ctor: Constructor<T_4>, nameOrOptions?: string | BindingFromClassOptions | undefined) => Binding<T_4>;
        servers: <T_5 extends Server>(ctors: Constructor<T_5>[]) => Binding<any>[];
        getServer: <T_6 extends Server>(target: string | Constructor<T_6>) => Promise<T_6>;
        start: () => Promise<void>;
        stop: () => Promise<void>;
        setMetadata: (metadata: ApplicationMetadata) => void;
        lifeCycleObserver: <T_7 extends LifeCycleObserver>(ctor: Constructor<T_7>, nameOrOptions?: string | BindingFromClassOptions | undefined) => Binding<T_7>;
        service: <S_2>(cls: Constructor<S_2 | Provider<S_2>>, nameOrOptions?: string | ServiceOptions | undefined) => Binding<S_2>;
        interceptor: (interceptor: Interceptor | Constructor<Provider<Interceptor>>, nameOrOptions?: string | InterceptorBindingOptions | undefined) => Binding<Interceptor>;
        readonly name: string;
        readonly subscriptionManager: ContextSubscriptionManager;
        readonly parent: Context | undefined;
        emitEvent: <T_8 extends ContextEvent>(type: string, event: T_8) => void;
        emitError: (err: unknown) => void;
        bind: <ValueType = any>(key: BindingAddress<ValueType>) => Binding<ValueType>;
        add: (binding: Binding<unknown>) => Application;
        configure: <ConfigValueType = any>(key?: string | BindingKey<unknown> | undefined) => Binding<ConfigValueType>;
        getConfigAsValueOrPromise: <ConfigValueType_1>(key: BindingAddress<unknown>, propertyPath?: string | undefined, resolutionOptions?: ResolutionOptions | undefined) => ValueOrPromise<ConfigValueType_1 | undefined>;
        getConfig: <ConfigValueType_2>(key: BindingAddress<unknown>, propertyPath?: string | undefined, resolutionOptions?: ResolutionOptions | undefined) => Promise<ConfigValueType_2 | undefined>;
        getConfigSync: <ConfigValueType_3>(key: BindingAddress<unknown>, propertyPath?: string | undefined, resolutionOptions?: ResolutionOptions | undefined) => ConfigValueType_3 | undefined;
        unbind: (key: BindingAddress<unknown>) => boolean;
        subscribe: (observer: ContextEventObserver) => Subscription;
        unsubscribe: (observer: ContextEventObserver) => boolean;
        close: () => void;
        isSubscribed: (observer: ContextObserver) => boolean;
        createView: <T_9 = unknown>(filter: BindingFilter, comparator?: BindingComparator | undefined) => ContextView<T_9>;
        contains: (key: BindingAddress<unknown>) => boolean;
        isBound: (key: BindingAddress<unknown>) => boolean;
        getOwnerContext: (key: BindingAddress<unknown>) => Context | undefined;
        find: <ValueType_1 = any>(pattern?: string | RegExp | BindingFilter | undefined) => Readonly<Binding<ValueType_1>>[];
        findByTag: <ValueType_2 = any>(tagFilter: string | RegExp | Record<string, any>) => Readonly<Binding<ValueType_2>>[];
        get: {
            <ValueType_3>(keyWithPath: BindingAddress<ValueType_3>, session?: ResolutionSession | undefined): Promise<ValueType_3>;
            <ValueType_4>(keyWithPath: BindingAddress<ValueType_4>, options: ResolutionOptions): Promise<ValueType_4 | undefined>;
        };
        getSync: {
            <ValueType_5>(keyWithPath: BindingAddress<ValueType_5>, session?: ResolutionSession | undefined): ValueType_5;
            <ValueType_6>(keyWithPath: BindingAddress<ValueType_6>, options?: ResolutionOptions | undefined): ValueType_6 | undefined;
        };
        getBinding: {
            <ValueType_7 = any>(key: BindingAddress<ValueType_7>): Binding<ValueType_7>;
            <ValueType_8>(key: BindingAddress<ValueType_8>, options?: {
                optional?: boolean | undefined;
            } | undefined): Binding<ValueType_8> | undefined;
        };
        findOrCreateBinding: <T_10>(key: BindingAddress<T_10>, policy?: BindingCreationPolicy | undefined) => Binding<T_10>;
        getValueOrPromise: <ValueType_9>(keyWithPath: BindingAddress<ValueType_9>, optionsOrSession?: ResolutionOptions | ResolutionSession | undefined) => ValueOrPromise<ValueType_9 | undefined>;
        toJSON: () => JSONObject;
        inspect: (options?: ContextInspectOptions | undefined) => JSONObject;
        addListener: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        on: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        once: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        prependListener: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        prependOnceListener: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        removeListener: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        off: (event: string | symbol, listener: (...args: any[]) => void) => Application;
        removeAllListeners: (event?: string | symbol | undefined) => Application;
        setMaxListeners: (n: number) => Application;
        getMaxListeners: () => number;
        listeners: (event: string | symbol) => Function[];
        rawListeners: (event: string | symbol) => Function[];
        emit: (event: string | symbol, ...args: any[]) => boolean;
        eventNames: () => (string | symbol)[];
        listenerCount: (type: string | symbol) => number;
    };
} & T;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  superClass | T |  |

<b>Returns:</b>

{ new (...args: any\[\]): { serviceProvider&lt;S&gt;(provider: [Constructor](./context.constructor.md)<!-- -->&lt;[Provider](./context.provider.md)<!-- -->&lt;S&gt;&gt;, nameOrOptions?: string \| [ServiceOptions](./core.serviceoptions.md) \| undefined): [Binding](./context.binding.md)<!-- -->&lt;S&gt;; component&lt;T\_1 extends [Component](./core.component.md) = [Component](./core.component.md)<!-- -->&gt;(componentCtor: [Constructor](./context.constructor.md)<!-- -->&lt;T\_1&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md) \| undefined): [Binding](./context.binding.md)<!-- -->&lt;T\_1&gt;; mountComponentServices&lt;T\_2 extends [Component](./core.component.md) = [Component](./core.component.md)<!-- -->&gt;(component: [Constructor](./context.constructor.md)<!-- -->&lt;T\_2&gt;, componentBindingKey?: string \| [BindingKey](./context.bindingkey.md)<!-- -->&lt;T\_2&gt; \| undefined): void; readonly options: [ApplicationConfig](./core.applicationconfig.md)<!-- -->; readonly state: string; controller: &lt;T\_3&gt;(controllerCtor: [Constructor](./context.constructor.md)<!-- -->&lt;T\_3&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;T\_3&gt;; server: &lt;T\_4 extends [Server](./core.server.md)<!-- -->&gt;(ctor: [Constructor](./context.constructor.md)<!-- -->&lt;T\_4&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;T\_4&gt;; servers: &lt;T\_5 extends [Server](./core.server.md)<!-- -->&gt;(ctors: [Constructor](./context.constructor.md)<!-- -->&lt;T\_5&gt;\[\]) =&gt; [Binding](./context.binding.md)<!-- -->&lt;any&gt;\[\]; getServer: &lt;T\_6 extends [Server](./core.server.md)<!-- -->&gt;(target: string \| [Constructor](./context.constructor.md)<!-- -->&lt;T\_6&gt;) =&gt; Promise&lt;T\_6&gt;; start: () =&gt; Promise&lt;void&gt;; stop: () =&gt; Promise&lt;void&gt;; setMetadata: (metadata: [ApplicationMetadata](./core.applicationmetadata.md)<!-- -->) =&gt; void; lifeCycleObserver: &lt;T\_7 extends [LifeCycleObserver](./core.lifecycleobserver.md)<!-- -->&gt;(ctor: [Constructor](./context.constructor.md)<!-- -->&lt;T\_7&gt;, nameOrOptions?: string \| [BindingFromClassOptions](./context.bindingfromclassoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;T\_7&gt;; service: &lt;S\_2&gt;(cls: [Constructor](./context.constructor.md)<!-- -->&lt;S\_2 \| [Provider](./context.provider.md)<!-- -->&lt;S\_2&gt;&gt;, nameOrOptions?: string \| [ServiceOptions](./core.serviceoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;S\_2&gt;; interceptor: (interceptor: [Interceptor](./context.interceptor.md) \| [Constructor](./context.constructor.md)<!-- -->&lt;[Provider](./context.provider.md)<!-- -->&lt;[Interceptor](./context.interceptor.md)<!-- -->&gt;&gt;, nameOrOptions?: string \| [InterceptorBindingOptions](./context.interceptorbindingoptions.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;[Interceptor](./context.interceptor.md)<!-- -->&gt;; readonly name: string; readonly subscriptionManager: [ContextSubscriptionManager](./context.contextsubscriptionmanager.md)<!-- -->; readonly parent: [Context](./context.context.md) \| undefined; emitEvent: &lt;T\_8 extends [ContextEvent](./context.contextevent.md)<!-- -->&gt;(type: string, event: T\_8) =&gt; void; emitError: (err: unknown) =&gt; void; bind: &lt;ValueType = any&gt;(key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType&gt;) =&gt; [Binding](./context.binding.md)<!-- -->&lt;ValueType&gt;; add: (binding: [Binding](./context.binding.md)<!-- -->&lt;unknown&gt;) =&gt; [Application](./core.application.md)<!-- -->; configure: &lt;ConfigValueType = any&gt;(key?: string \| [BindingKey](./context.bindingkey.md)<!-- -->&lt;unknown&gt; \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;ConfigValueType&gt;; getConfigAsValueOrPromise: &lt;ConfigValueType\_1&gt;(key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;, propertyPath?: string \| undefined, resolutionOptions?: [ResolutionOptions](./context.resolutionoptions.md) \| undefined) =&gt; [ValueOrPromise](./context.valueorpromise.md)<!-- -->&lt;ConfigValueType\_1 \| undefined&gt;; getConfig: &lt;ConfigValueType\_2&gt;(key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;, propertyPath?: string \| undefined, resolutionOptions?: [ResolutionOptions](./context.resolutionoptions.md) \| undefined) =&gt; Promise&lt;ConfigValueType\_2 \| undefined&gt;; getConfigSync: &lt;ConfigValueType\_3&gt;(key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;, propertyPath?: string \| undefined, resolutionOptions?: [ResolutionOptions](./context.resolutionoptions.md) \| undefined) =&gt; ConfigValueType\_3 \| undefined; unbind: (key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;) =&gt; boolean; subscribe: (observer: [ContextEventObserver](./context.contexteventobserver.md)<!-- -->) =&gt; [Subscription](./context.subscription.md)<!-- -->; unsubscribe: (observer: [ContextEventObserver](./context.contexteventobserver.md)<!-- -->) =&gt; boolean; close: () =&gt; void; isSubscribed: (observer: [ContextObserver](./context.contextobserver.md)<!-- -->) =&gt; boolean; createView: &lt;T\_9 = unknown&gt;(filter: [BindingFilter](./context.bindingfilter.md)<!-- -->, comparator?: [BindingComparator](./context.bindingcomparator.md) \| undefined) =&gt; [ContextView](./context.contextview.md)<!-- -->&lt;T\_9&gt;; contains: (key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;) =&gt; boolean; isBound: (key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;) =&gt; boolean; getOwnerContext: (key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;unknown&gt;) =&gt; [Context](./context.context.md) \| undefined; find: &lt;ValueType\_1 = any&gt;(pattern?: string \| RegExp \| [BindingFilter](./context.bindingfilter.md) \| undefined) =&gt; Readonly&lt;[Binding](./context.binding.md)<!-- -->&lt;ValueType\_1&gt;&gt;\[\]; findByTag: &lt;ValueType\_2 = any&gt;(tagFilter: string \| RegExp \| Record&lt;string, any&gt;) =&gt; Readonly&lt;[Binding](./context.binding.md)<!-- -->&lt;ValueType\_2&gt;&gt;\[\]; get: { &lt;ValueType\_3&gt;(keyWithPath: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_3&gt;, session?: [ResolutionSession](./context.resolutionsession.md) \| undefined): Promise&lt;ValueType\_3&gt;; &lt;ValueType\_4&gt;(keyWithPath: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_4&gt;, options: [ResolutionOptions](./context.resolutionoptions.md)<!-- -->): Promise&lt;ValueType\_4 \| undefined&gt;; }; getSync: { &lt;ValueType\_5&gt;(keyWithPath: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_5&gt;, session?: [ResolutionSession](./context.resolutionsession.md) \| undefined): ValueType\_5; &lt;ValueType\_6&gt;(keyWithPath: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_6&gt;, options?: [ResolutionOptions](./context.resolutionoptions.md) \| undefined): ValueType\_6 \| undefined; }; getBinding: { &lt;ValueType\_7 = any&gt;(key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_7&gt;): [Binding](./context.binding.md)<!-- -->&lt;ValueType\_7&gt;; &lt;ValueType\_8&gt;(key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_8&gt;, options?: { optional?: boolean \| undefined; } \| undefined): [Binding](./context.binding.md)<!-- -->&lt;ValueType\_8&gt; \| undefined; }; findOrCreateBinding: &lt;T\_10&gt;(key: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;T\_10&gt;, policy?: [BindingCreationPolicy](./context.bindingcreationpolicy.md) \| undefined) =&gt; [Binding](./context.binding.md)<!-- -->&lt;T\_10&gt;; getValueOrPromise: &lt;ValueType\_9&gt;(keyWithPath: [BindingAddress](./context.bindingaddress.md)<!-- -->&lt;ValueType\_9&gt;, optionsOrSession?: [ResolutionOptions](./context.resolutionoptions.md) \| [ResolutionSession](./context.resolutionsession.md) \| undefined) =&gt; [ValueOrPromise](./context.valueorpromise.md)<!-- -->&lt;ValueType\_9 \| undefined&gt;; toJSON: () =&gt; [JSONObject](./context.jsonobject.md)<!-- -->; inspect: (options?: [ContextInspectOptions](./context.contextinspectoptions.md) \| undefined) =&gt; [JSONObject](./context.jsonobject.md)<!-- -->; addListener: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; on: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; once: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; prependListener: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; prependOnceListener: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; removeListener: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; off: (event: string \| symbol, listener: (...args: any\[\]) =&gt; void) =&gt; [Application](./core.application.md)<!-- -->; removeAllListeners: (event?: string \| symbol \| undefined) =&gt; [Application](./core.application.md)<!-- -->; setMaxListeners: (n: number) =&gt; [Application](./core.application.md)<!-- -->; getMaxListeners: () =&gt; number; listeners: (event: string \| symbol) =&gt; Function\[\]; rawListeners: (event: string \| symbol) =&gt; Function\[\]; emit: (event: string \| symbol, ...args: any\[\]) =&gt; boolean; eventNames: () =&gt; (string \| symbol)\[\]; listenerCount: (type: string \| symbol) =&gt; number; }; } &amp; T

## Example


```ts
class MyApplication extends ServiceMixin(Application) {}

```
Please note: the members in the mixin function are documented in a dummy class called <a href="#ServiceMixinDoc">ServiceMixinDoc</a>


