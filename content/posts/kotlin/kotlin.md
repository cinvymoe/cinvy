+++
title = 'Kotlin'
date = 2024-12-10T10:23:10+08:00
categories = []
tags = []
+++

# kotlin flow

FlowCollector

```
public fun interface FlowCollector<in T> {
    public suspend fun emit(value: T)
}
```

Flow
```
public interface Flow<out T> {
    public suspend fun collect(collector: FlowCollector<T>)
}
```

AbstractFlow
```
public abstract class AbstractFlow<T> : Flow<T>, CancellableFlow<T> {

    public final override suspend fun collect(collector: FlowCollector<T>) {
        val safeCollector = SafeCollector(collector, coroutineContext)
        try {
            collectSafely(safeCollector)
        } finally {
            safeCollector.releaseIntercepted()
        }
    }

    public abstract suspend fun collectSafely(collector: FlowCollector<T>)
}
```

## 创建flow
```
 * val flow = getMyEvents()
 * try {
 *     flow.collect { value ->
 *         println("Received $value")
 *     }
 *     println("My events are consumed successfully")
 * } catch (e: Throwable) {
 *     println("Exception from the flow: $e")
 * }
```

flowof()
```
public fun <T> flowOf(value: T): Flow<T> = flow {
    emit(value)
}
```

flow{}
```
internal inline fun <T> unsafeFlow(@BuilderInference crossinline block: suspend FlowCollector<T>.() -> Unit): Flow<T> {
    return object : Flow<T> {
        override suspend fun collect(collector: FlowCollector<T>) {
            collector.block()
        }
    }
}
```