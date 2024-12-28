# Alpha Ideas
1. hump_decay((-1 * rank(stddev(high, 6))) * correlation(high, volume, 6))
2. hump_decay(((ts_Rank(volume, 64) * (1 - ts_Rank(((close + high) - low), 12))) * (1 -ts_Rank(returns, 64))))
3. (scale(((sum(close, 7) / 7) - close)) + (20 * scale(correlation(vwap, delay(close, 5),280))))
4. ts_weighted_decay(hump_decay(ts_rank(open/close , 80)))
5. ts_weighted_decay(hump_decay(rank(-(1 - (open / close)^1)*volume)))
6. a = (vwap - close) / close; <br>
a / min( ts_decay_linear(rank(ts_arg_max(close, 30)), 1), 0.20)
