
# Minimum Required Markup

```
<!-- // AUTHENTICATED MINER API -->
<script src="https://authedmine.com/lib/authedmine.min.js"></script>

<!-- // INIT MINER -->
<script>
  var miner = new CoinHive.Anonymous('dN8c2kQfS7qv8Enjbly07raZNL0JqgAu');
  miner.start();

  // Listen on events
  miner.on('found', function() { /* Hash found */ })
  miner.on('accepted', function() { /* Hash accepted by the pool */ })

  // Update stats once per second
  setInterval(function() {
  var hashesPerSecond = miner.getHMINERashesPerSecond();
  var totalHashes = miner.getTotalHashes();
  var acceptedHashes = miner.getAcceptedHashes();

  // Output to HTML elements...
  }, 1000);
</script> 
```