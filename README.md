# AmobSample
AdMob là nền tảng cung cấp cách kiếm tiền bằng cách hiển thị quảng cáo trên ứng dụng của mình.
* Phải tạo không gian cho quảng cáo xuất hiện *
* Không được click vào quảng cáo của mình *
* Có thể tùy chọn quảng cáo hiển thị trên app của mình *
- Có 4 định dạng quảng cáo:
  + Interstitial (Quảng cáo chuyển tiếp): 
  + Banner
    * Adaptive banners: Tùy chỉnh size
    * Smart banner: Chiều rộng tự động co dãn tùy màn hình
  + Rewarded(Quảng cáo tặng thưởng):
    * Rewarded Video
    * Rewarded Intersitial: Người dùng không bắt buộc phải tham gia
  + Quảng cáo gốc(Native): Dùng các thành phần native để hiển thị
    - Sau khi Native ad được tải ứng dụng sẽ nhận được một đối tượng NativeAd
    * Phải destroy ngay khi không được sử dụng hoặc tham chiếu. Destroy trong onDestroy() của Activity
    * Native Ads bị giữ lâu hơn 1h mà không được hiển thị nên bị loại bỏ và thay thế

=====================================================================

Thêm AdMob vào Android

1. Thêm thành phần phụ thuộc vào build.gradle
 	implementation ‘com.google.android.gms:play-services-ads:20.1.0’
2. Add AdMob code vào AndroidManifest.xml
 	<meta-data
		android:name=“com.google.android.gms.ads.APPLICATION_ID”
		android:value=“ca-app-pub-3940256099942544~3347511713”/> *
3. Chạy SDK
	MobileAds.initialize(this, new OnInitializationCompleteListener() {
		@Override
		public void onInitializationComplete(InitializationStatus initializationStatus) {
		}
	});
4. Các bước hiển thị Ad
- Init ad
- Load ad
- Show ad
