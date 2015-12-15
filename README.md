# ImportantBrowsers
JS HACK for Common Browsers

You can use it as much you want

        // if ie_ver() gives you version of ie
        function ie_ver() {
            var iev = 0;
            var ieold = (/MSIE (\d+\.\d+);/.test(navigator.userAgent));
            var trident = !!navigator.userAgent.match(/Trident\/7.0/);
            var rv = navigator.userAgent.indexOf("rv:11.0");
            if (ieold) iev = new Number(RegExp.$1);
            if (navigator.appVersion.indexOf("MSIE 10") != -1) iev = 10;
            if (trident && rv != -1) iev = 11;

            return iev;
        }
        // Other browser check
        var is_chrome = navigator.userAgent.indexOf('Chrome') > -1;
        var is_explorer = navigator.userAgent.indexOf('MSIE') > -1;
        var is_firefox = navigator.userAgent.indexOf('Firefox') > -1;
        var is_safari = navigator.userAgent.indexOf("Safari") > -1;
        var is_opera = navigator.userAgent.toLowerCase().indexOf("op") > -1;
        if (is_chrome && is_safari) {
            is_safari = false;
        }
        if (is_chrome && is_opera) {
            is_chrome = false;
        }
        
        // Check if device is mobile
        var isMobile = (/iphone|ipad|ipod|android|blackberry|mini|windows\sce|palm/i.test(navigator.userAgent.toLowerCase()));
        // If screen orientation changes
        $(window).on('orientationchange', function (event) {
                //location.reload();
        });

