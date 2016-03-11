package kr.co.nowcom.mobile.afreeca.marshmallow;
import android.app.Activity;
import android.content.Context;

public class MLibDelegator {
	
	public static class Settings {
		
		public static final String ACTION_MANAGE_OVERLAY_PERMISSION = android.provider.Settings.ACTION_MANAGE_OVERLAY_PERMISSION;
		public static final String ACTION_MANAGE_WRITE_SETTINGS = android.provider.Settings.ACTION_MANAGE_WRITE_SETTINGS;

		public static boolean canDrawOverlays(Context context) {
			if(android.os.Build.VERSION.SDK_INT < android.os.Build.VERSION_CODES.M){
				return true;
			}
			return android.provider.Settings.canDrawOverlays(context);
		}
		
		public static class System {
			public static boolean canWrite(Context context) {
				if(android.os.Build.VERSION.SDK_INT < android.os.Build.VERSION_CODES.M){
					return true;
				}
				return android.provider.Settings.System.canWrite(context);
			}
		}
	}

	public static class ActivityCompat {
		public static int checkSelfPermission(Context context, String permission) {
			return android.support.v4.app.ActivityCompat.checkSelfPermission(context, permission);
		}
		
		public static boolean shouldShowRequestPermissionRationale(Activity activity, String permission) {
			return android.support.v4.app.ActivityCompat.shouldShowRequestPermissionRationale(activity, permission);
		}
		
		public static void requestPermissions(Activity activity, String[] permissions, int requestCode) {
			android.support.v4.app.ActivityCompat.requestPermissions(activity, permissions, requestCode);
		}
	}
}
