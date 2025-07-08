# HFT Engineer Track: 90-Day Schedule

## Core Idea and Ethos

> **The HFT Engineer Track is a disciplined, modular, and performance-driven systems challenge.**  
In 90 days, you’ll **build out a full real-time trading infrastructure**, one tested module at a time.  
Each module is:
- **Composable** — it plugs into other modules.
- **Memory-safe** — no leaks, no undefined behavior.
- **Low-latency** — favor lock-free, zero-copy, and bounded constructs.
- **Observable** — logs, metrics, and debug hooks matter.
- **Professional** — validated by `GTest`, Valgrind, and clean CMake structure.

This track prepares you for the **actual job** of writing and maintaining critical infrastructure at a high-frequency trading firm — **not just passing interviews**.

---

## WEEK 1–3: Infrastructure and Data Arteries

| Day | Module |
|-----|--------|
| 1   | Tick and Order structs with strong types |
| 2   | TickQueue<T> — thread-safe bounded blocking queue |
| 3   | TickDispatcher — route tick to strategy, observers |
| 4   | OrderRouter — print or dispatch orders safely |
| 5   | Strategy interface — pure virtual base |
| 6   | MomentumStrategy — basic tick-based market entry |
| 7   | OrderObserver and TickObserver interfaces |
| 8   | TickLogger and OrderLogger — observer implementations |
| 9   | RiskMonitor — tick-based alerting system |
| 10  | RingBuffer<T> — blocking circular buffer with shutdown |
| 11  | MemoryArena — aligned fixed-size memory pool |
| 12  | SharedPtrWithDeleter — wrap arena objects safely |
| 13  | GTest and Valgrind verification for MemoryArena |
| 14  | ReusePoolAllocator<T> — STL-compatible object pool |
| 15  | ProducerThread — tick generator using MemoryArena |
| 16  | ConsumerThread — tick processor using dispatcher |
| 17  | DoubleBuffer<T> — lock-free state swap pattern |
| 18  | ThreadAffinity module — pin threads to cores |
| 19  | StatsTracker — atomic counters, latencies |
| 20  | SimTickGenerator — replayer with timestamp pacing |

---

## WEEK 4–6: Module Lifecycle + Application Wiring

| Day | Module |
|-----|--------|
| 21  | ModuleBase — start/stop/init hooks with threading |
| 22  | ModuleGraph — dependency-aware initialization DAG |
| 23  | ThreadedModule<T> — run any module in its own thread |
| 24  | LogModule — centralized async logger |
| 25  | MetricsModule — collect counters, stats per module |
| 26  | SnapshotStore<T> — store periodic system snapshots |
| 27  | RollingStatsWindow<T> — time-window stats tracking |
| 28  | RateLimiter — fixed-window and token-bucket modes |
| 29  | CircuitBreaker — trip on internal failures |
| 30  | BackpressureGuard — pause upstream if queue fills |
| 31  | AsyncCallbackRouter — register + dispatch callbacks |
| 32  | RemoteCommandRouter — command line interface to system |
| 33  | RollingMeanStdDev<T> — thread-safe running stats |
| 34  | LatencyHistogram — bucketed latency tracker |
| 35  | SimClock — simulated time control for testing |
| 36  | RateAdaptivePoller — adjust poll rate based on message load |
| 37  | ModuleRegistry — register and lookup modules globally |
| 38  | LiveStateKVStore — shared key-value state per module |
| 39  | HealthMonitor — checks module liveliness periodically |
| 40  | ShutdownManager — coordinated shutdown across system |

---

## WEEK 7–9: Trading Strategy and Book Infrastructure

| Day | Module |
|-----|--------|
| 41  | OrderBookLevel — L1 bid/ask tracking |
| 42  | OrderBookL2 — full depth, price+qty map |
| 43  | VWAPCalculator — weighted price observer |
| 44  | MedianTracker — streaming median with heaps |
| 45  | TradeRateLimiter — enforce per-symbol trade cap |
| 46  | PriceJumpDetector — flag large price gaps |
| 47  | MovingAverage<T> — sliding MA per symbol |
| 48  | ExecutionThrottler — slow down order send rate |
| 49  | SnapshotPublisher — write state to disk safely |
| 50  | StrategyLoader — dynamically select strategy from config |
| 51  | MarketCloseHandler — auto shutdown on market close |
| 52  | InventoryTracker — position tracking per symbol |
| 53  | FairValueEstimator — compute expected price via VWAP/book |
| 54  | TradeBlotter — journal of executed trades |
| 55  | SessionManager — tracks trading sessions |
| 56  | PnLCalculator — live unrealized + realized PnL |
| 57  | SymbolRouter — per-symbol strategy routing |
| 58  | OrderRateProfiler — monitor order frequency and latency |
| 59  | TradeReconciler — match local trades with fill reports |
| 60  | AnomalyDetector — flag bad ticks or stale data |

---

## WEEK 10–13: Full-System Behavior + Testing

| Day | Module |
|-----|--------|
| 61  | TickReplayer — replay historical data |
| 62  | LiveTickMuxer — multiplex tick streams from multiple sources |
| 63  | FeedDropDetector — alert on tick silence |
| 64  | OutlierGuard — suppress extreme ticks temporarily |
| 65  | SyntheticTickInjector — simulate spikes |
| 66  | MockOrderRouter — test-only order routing |
| 67  | TestModuleDriver — run tests in module graph |
| 68  | TraceLogger — append all module state changes |
| 69  | DeadlockDetector — monitor stuck threads via heartbeat |
| 70  | TimingProfiler — log time between key module calls |
| 71  | SimulatedExchange — simulate fills, rejects, cancels |
| 72  | MatchingEngineSim — simulate internal exchange for backtesting |
| 73  | GTestExtension — custom matchers for module graph testing |
| 74  | ValgrindSafeRunner — leak-free test runner |
| 75  | FakeClockInjector — inject testable time into modules |
| 76  | LoadTester — flood system with ticks/orders and measure latency |
| 77  | SystemDebuggerCLI — interactively poke modules |
| 78  | SnapshotComparer — diff snapshots over time |
| 79  | TickIntegrityChecker — validate tick feed consistency |
| 80  | FlushOnDemand — flush state/logs/metrics with signal |

---

## WEEK 14–15: Capstone + Real Deployment Scenarios

| Day | Module |
|-----|--------|
| 81  | ReplayOrLiveSwitcher — switch between modes dynamically |
| 82  | LiveFeedMonitor — plug into live socket or file feed |
| 83  | RealTimeMetricsUploader — send stats to remote server |
| 84  | CrashRecoveryManager — restore from snapshot |
| 85  | BuildSystemRefactor — clean up CMake + test harness |
| 86  | DeploymentSanityCheck — verify live config, state |
| 87  | EmergencyKillSwitch — halt on risk breach |
| 88  | ModuleDocsGenerator — auto-doc module APIs |
| 89  | Final Integration Test — full graph under stress |
| 90  | Capstone Demo Day — Deploy full system, run live ticks, log orders, walk through design for CTO audience |
