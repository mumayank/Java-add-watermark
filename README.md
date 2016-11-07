# Java add watermark
This method accepts a bitmap, applies a watermark on it at a selected location on the bitmap, and returns the edited bitmap.

    private Bitmap addWaterMark(Bitmap src) {
        int w = src.getWidth();
        int h = src.getHeight();
        Bitmap result = Bitmap.createBitmap(w, h, src.getConfig());
        Canvas canvas = new Canvas(result);
        canvas.drawBitmap(src, 0, 0, null);

        Bitmap waterMark = BitmapFactory.decodeResource(getResources(), R.drawable.watermark);
        canvas.drawBitmap(waterMark, 0, 0, null);

        return result;
    }
