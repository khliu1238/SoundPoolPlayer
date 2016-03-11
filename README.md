# SoundPoolPlayer
custom extention from Android SoundPool with setOnCompletionListener without the low-efficiency drawback of MediaPlayer

usage: similar to MediaPlayer except load()

creation:
  SoundPoolPlayer mPlayer = SoundPoolPlayer.create(context, resId);
  mPlayer.setOnCompletionListener(
  	new MediaPlayer.OnCompletionListener() {
	        @Override
	        public void onCompletion(MediaPlayer mp) {
	        	Log.d("debug", "completed");
	        }
		};
  );
  mPlayer.load(new SoundPool.OnLoadCompleteListener() {
		@Override
		public void onLoadComplete(SoundPool soundPool, int sampleId, int status) {
			mPlayer.play();
		}
	});

pause:
	mPlayer.pause();

stop:
	mPlayer.stop();

resume:
	mPlayer.resume();

isPlaying:
	mPlayer.isPlaying();



