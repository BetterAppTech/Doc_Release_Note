# BetterApp Ad SDK Release Notes

## com.betterapp.sdk:ads:3.0.0.0

### 📝 修改点摘要
1. 升级主要广告网络 SDK 版本
2. 重构广告埋点逻辑，支持离线场景展示广告
3. 热启动时广告预拉取优化，在 `AdConfigFetcher` 中新增 `reLoadAd()` 接口
4. 精简 UMP 集成方式，可选择统一调用 `MediaAdLoader.checkUMP(...)`

---

### 1. 升级主要广告网络 SDK 版本
- AdMob: 23.5 → 24.2
- Meta (Facebook): 6.18.0 → 6.19.0
- AppLovin MAX: 13.0.1 → 13.2.0
- Pangle: 6.2.0.7 → 7.1.1.3
- Vungle (Liftoff): 7.4.1 → 7.4.3
- DT Exchange: 8.3.3 → 8.3.7
- PubMatic: 4.4.0 → 4.5.1
- Verve: 3.1.0 → 3.3.0
- Smaato: 22.7.1 → 22.7.2

---

### 2. 重构广告埋点逻辑，支持离线场景展示广告
- 更新 `MediaAdLoader.isAdComeNetworkOpen(...)` 方法逻辑
- 无网络时不再阻断广告展示，依赖本地缓存素材实现离线广告播放

---

### 3. 热启动时广告预拉取优化，在 `AdConfigFetcher` 中新增 `reLoadAd()` 接口
- 提供触发热启动时广告预拉取的入口，适用于用户长时间离开应用后返回的二次拉取

```java
@Override
public void reLoadAd() {
    if (initAdReady) {
        preloadAd(activity, RT_SPLASH_INTER);
        preloadAd(activity, RT_BANNER);
        preloadAd(activity, Constants.RT_MREC);
        preloadAd(activity, Constants.RT_OPEN_ADS);
    }
}
```

### 4.精简 UMP 集成方式
- 客户端依然可以维持原有方案实现UMP，也可选择统一调用 `MediaAdLoader.checkUMP(...)`，统一埋点上报与后续UMP规则更新


👉 [See All Release Notes](./ad_sdk_release_note.md)

