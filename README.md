# SoundPoolPlayer
custom extention from Android SoundPool with setOnCompletionListener without the low-efficiency drawback of MediaPlayer.

## creation:

	SoundPoolPlayer mPlayer = SoundPoolPlayer.create(context, resId);
	mPlayer.setOnCompletionListener(
		new MediaPlayer.OnCompletionListener() {
	        @Override
	        public void onCompletion(MediaPlayer mp) { 	//mp will be null here
	        	Log.d("debug", "completed");
	        }
		};
	);
	mPlayer.play()

## pause:

    mPlayer.pause();

## stop:

    mPlayer.stop();

## resume:

    mPlayer.resume();

## isPlaying:

    mPlayer.isPlaying();
