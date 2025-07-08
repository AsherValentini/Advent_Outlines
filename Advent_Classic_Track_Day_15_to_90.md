# Advent of Modules: Classic Track (Day 15–90)

## Ethos and Design

> **This track is about building sharpness under pressure.**  
You get 45–60 minutes to solve a C++ challenge from scratch. Each challenge is:
- **Interview-realistic** — you'd get this in a paired round.
- **Tactically scoped** — not a full system, but not a toy.
- **Focused** on DSA, recursion, STL tricks, memory, or OOP.
- **Self-contained** — no reuse, no scaffolding.
- A mix of **HFT-relevant patterns** and **clever system-inspired problems**.

---

## 🔹 Week 3: Core Containers + Memory Tricks

| Day | Challenge |
|-----|-----------|
| 15  | `SPSCQueue<T>` — lock-free, single-producer/single-consumer queue |
| 16  | `SmartPtrPuzzle` — implement a basic shared_ptr with ref counting |
| 17  | `FixedCapacitySet<T>` — no heap, all in stack or buffer |
| 18  | `ByteView` — view-only wrapper over raw bytes (like std::span) |
| 19  | `PlacementFactory` — placement-new + object registry |
| 20  | `DynamicArenaSplit` — arena that allows slice-based sub-allocations |
| 21  | `MaxSizeCache` — LRU eviction with map + list combo |

---

## 🔹 Week 4: Graphs, Maps, Prefix Trees

| Day | Challenge |
|-----|-----------|
| 22  | `BoxMergeApprox` — revisit bounding boxes with union-find merge |
| 23  | `CraftingRecursion` — object factory (enum class) via recursive crafting |
| 24  | `FileSystemTree<T>` — simulate mkdir, ls, cd using trie |
| 25  | `DFSRecursor` — recursion over graph with cycle check |
| 26  | `IDCompressor` — map sparse user IDs to compact 0-N IDs |
| 27  | `InMemoryKVStoreV2` — support range queries with ordered map |
| 28  | `JSONPathFinder` — parse simple JSON & extract paths to values |

---

## 🔹 Week 5: Allocation, Cloning, Flyweight

| Day | Challenge |
|-----|-----------|
| 29  | `ClonableShapeSystem` — base + derived polymorphic clone via virtual clone() |
| 30  | `FlyweightStringPool` — deduplicate string instances |
| 31  | `ArenaObjectFactory` — create objects using tag + arena allocation |
| 32  | `CloneGraph` — classic Leetcode-style graph deep copy |
| 33  | `ObjectVersioner` — store immutable copies of object on update |
| 34  | `CompactVector<T>` — fallback from stack buffer to heap |
| 35  | `PathResolver` — collapse `..`, `.`, `/` in path from scratch |

---

## 🔹 Week 6: Enum Models + Event Logic

| Day | Challenge |
|-----|-----------|
| 36  | `SignalDispatcher` — emit signals to registered callbacks |
| 37  | `EnumVisitor` — visit enum values using match-style switch |
| 38  | `OrderStateMachine` — enum-based transitions for order lifecycle |
| 39  | `MarketSimulator` — enum + tick-based logic for fill, reject |
| 40  | `TimerQueue` — time-prioritized task execution (min-heap) |
| 41  | `RetryPolicy` — exponential backoff logic (stateful object) |
| 42  | `TaskExecutor` — run N tasks in sequence + support cancellation |

---

## 🔹 Week 7: Recursion, Object Graphs, and Parsing

| Day | Challenge |
|-----|-----------|
| 43  | `FileSystemSize` — recurse directory tree and sum sizes |
| 44  | `BracketMatcher` — recursion stack to check nested brackets |
| 45  | `ExprEvaluator` — parse & evaluate arithmetic expression tree |
| 46  | `TagBasedMemoryStore` — allocate objects grouped by enum tag |
| 47  | `RegexMiniEngine` — recursive matcher for a*b?c+-like strings |
| 48  | `TypeErasedCommand` — run heterogeneous commands via base ptr |
| 49  | `SymbolTrieMatcher` — map tickers to symbols using compressed trie |

---

## 🔹 Week 8: STL Reinvention + Access Patterns

| Day | Challenge |
|-----|-----------|
| 50  | `CircularDeque<T>` — double-ended ring buffer |
| 51  | `MovingMedian<T>` — O(log n) via two heaps |
| 52  | `StreamSampler<T>` — sample 1-in-N randomly from stream |
| 53  | `JoinIterators` — zip/join multiple iterators together |
| 54  | `PagedAllocator` — batch-allocate from memory pages |
| 55  | `PathBacktracker` — return to previous steps via stack |
| 56  | `RangePartitioner` — divide [a, b] into evenly spaced buckets |

---

## 🔹 Week 9: Tick Systems + Real-Time Thinking

| Day | Challenge |
|-----|-----------|
| 57  | `TickDeduplicator` — suppress duplicate ticks with TTL |
| 58  | `MovingVWAP` — time-decayed volume-weighted avg price |
| 59  | `TradeFilter` — filter ticks by side, price, time |
| 60  | `TickCompressor` — combine low-res tick stream in-place |
| 61  | `TickAligner` — realign out-of-order ticks into buckets |
| 62  | `RiskGuard` — prevent trades above price/volume limits |
| 63  | `TradeRecorder` — log trades into CSV using RAII |

---

## 🔹 Week 10: Sandbox Architectures + Plugins

| Day | Challenge |
|-----|-----------|
| 64  | `PluginBase` — plugin interface + loader via registry map |
| 65  | `RuntimeStrategySelector` — switch strategies on the fly |
| 66  | `ModuleLifecycle` — init/start/stop/reset FSM |
| 67  | `ComponentGraph` — DAG of module dependencies |
| 68  | `SymbolPartitionRouter` — route by symbol hash |
| 69  | `StrategyConfigLoader` — read strategy params from JSON |
| 70  | `ZeroCopyPacketView` — read-only byte-slice accessor |

---

## 🔹 Week 11: Heaps, Maps, Stats, Locks

| Day | Challenge |
|-----|-----------|
| 71  | `TopKHeap` — track top K elements in stream |
| 72  | `AtomicHistogram` — thread-safe latency buckets |
| 73  | `StreamEntropyEstimator` — entropy estimator of stream |
| 74  | `RollingBitmask` — 64-bit window for booleans |
| 75  | `TTLMap` — key expires after N seconds |
| 76  | `SharedMutexMap` — read-heavy concurrent access |
| 77  | `StreamJoiner` — join on timestamp field across feeds |

---

## 🔹 Week 12: Mixed Mode Challenges

| Day | Challenge |
|-----|-----------|
| 78  | `MultimapInverter` — flip map<string, vector<int>> to int→string |
| 79  | `EnumHasher` — custom hash for enum class keys |
| 80  | `DependencyOrderer` — topological sort of modules |
| 81  | `StringInterner` — assign ID to each string, dedup |
| 82  | `CustomOptional<T>` — own optional type with has_value, value |
| 83  | `ObserverSet<T>` — subscribe/unsubscribe mechanism |
| 84  | `ReentrantLockGuard` — manual recursive lock wrapper |

---

## 🔹 Week 13: Final Stretch – Memory & Real-World Logic

| Day | Challenge |
|-----|-----------|
| 85  | `TimeSeriesCompactor` — flatten time-series into sparse bins |
| 86  | `StreamWindow<T>` — peek N before and after current element |
| 87  | `AlignedAllocator` — allocate 64B-aligned objects |
| 88  | `ThreadSafeBufferPool` — bounded pool with blocking semantics |
| 89  | `MinimalFuture<T>` — promise/future one-shot value passing |
| 90  | **Final Boss** — design & build a `MarketDataRecorder` (dedup, flush, match) from scratch in 60 mins |
