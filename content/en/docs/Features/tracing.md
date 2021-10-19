---
title: Tracing
description: How Kiali integrates Distributed Tracing with Jaeger.
weight: 4
---

Kiali offers a native integration with Jaeger for Distributed Tracing.  As such, users can access Jaeger's trace visualizations.  But more
than that, Kiali incorporates tracing into several correlated views, making your investment in trace data even more valuable.

For a quick glimpse at Kiali tracing features, see below.  For a detailed explanation of tracing in Kiali, see this 3-part
[Trace my mesh](https://medium.com/kialiproject/trace-my-mesh-part-1-3-35e252f9c6a9) blog series,

<br />

## Workload detail

When investigating a workload, click the _Traces_ tab to visualize your traces in a chart. When selecting a trace Kiali
presents a tab for trace detail, and a tab for span details.  Kiali always tries to surface problem areas, Kiali uses a
heatmap approach to help the user identify problem traces or spans.

![Trace detail](/images/documentation/features/trace-detail.png)
![Span detail](/images/documentation/features/trace-span-detail.png)


## Metric Correlation

Kiali offers span overlays on Metric charts.  The user can simply enable the `spans` option to generate the overlay.  Clicking any
span will navigate back to the _Traces_ tab, focused on the trace of interest.

![Metrics with Tracing](/images/documentation/features/trace-metric-overlay.png)


## Graph Correlation

Kiali users often use the [Graph Feature](#topology) to visualize their mesh traffic.  In the side panel, When selecting a graph node,
the user will be presented with a _Traces_ tab, which lists available traces for the time period.  When selecting a trace the graph
will display an overlay for the trace's spans.  And the side panel will display span details and offer links back to the trace detail
views.

![Graph with Tracing](/images/documentation/features/trace-graph-overlay.png)


## Logs Correlation

Kiali works to correlate the standard _pillars of observability_: traces, metrics and logs. Kiali can present a unified view of
log and trace information, in this way letting users use logs to identify traces of interest.  When enabling the `spans` option
Kiali adds trace entries to the workload logs view.  Below, in time-sorted order, the user is presented with a unified view of application
logs (in white), Envoy proxy logs (in gold), and trace spaces (in blue).  Clicking a span of interest brings you to the detail
view for the trace of interest.

![Logs with Tracing](/images/documentation/features/trace-logs.png)
