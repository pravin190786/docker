
from(bucket: "mon_test")
    |> range(start: -15m)
    |> filter(fn: (r) => r._measurement == "cpu" and r._field == "usage_idle" and r.cpu == "cpu-total")
    |> yield()