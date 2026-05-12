# InventorySim

Simulates an single-warehouse inventory management system that handles these 
edge cases by preventing inventory oversells under load.

## Problem

Inventory management systems are an intriguing area for system designs. They
must follow strict rules for how inventory is added, removed, and transferred
between locations in a warehouse. Without careful handling, stock can be
purchased that doesn't exist.

For instance, a high traffic item can sell out quickly, but how can you prevent
two users from purchasing the last item at the same time? Race conditions happen
when multiple requests read and write the same inventory row at the same time.
Two customers can read only one unit of milk is available, both reserve it, and
the system oversells.
