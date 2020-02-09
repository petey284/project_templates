

### Bootstrap Template

Add to top:

  <meta charset="utf-8" />
  <link rel="apple-touch-icon" sizes="76x76" href="~/assets/img//apple-icon.png">
  <link rel="icon" type="image/png" href="~/assets/img//favicon.png">
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
  <title>
    My Template
  </title>
  <meta content='width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0, shrink-to-fit=no' name='viewport' />
  <!--     Fonts and icons     -->
  <link href="https://fonts.googleapis.com/css?family=Montserrat:400,700,200" rel="stylesheet" />
  <link href="https://maxcdn.bootstrapcdn.com/font-awesome/latest/css/font-awesome.min.css" rel="stylesheet">
  <!-- CSS Files -->
  <link href="~/assets/css/bootstrap.min.css" rel="stylesheet" />
  <link href="~/assets/css/paper-kit.css?v=2.2.0" rel="stylesheet" />

Adding the directory and then this section at the bottom.

    <script src="~/assets/js/core/jquery.min.js" type="text/javascript"></script>
    <script src="~/assets/js/core/popper.min.js" type="text/javascript"></script>
    <script src="~/assets/js/core/bootstrap.min.js" type="text/javascript"></script>

    <!--  Plugin for Switches, full documentation here: http://www.jque.re/plugins/version3/bootstrap.switch/ -->
    <script src="~/assets/js/plugins/bootstrap-switch.js"></script>


    <!--  Plugin for the Sliders, full documentation here: http://refreshless.com/nouislider/ -->
    <script src="~/assets/js/plugins/nouislider.min.js" type="text/javascript"></script>


    <!--  Plugin for the DatePicker, full documentation here: https://github.com/uxsolutions/bootstrap-datepicker -->
    <script src="~/assets/js/plugins/moment.min.js"></script>
    <script src="~/assets/js/plugins/bootstrap-datepicker.js" type="text/javascript"></script>


    <!-- Control Center for Paper Kit: parallax effects, scripts for the example pages etc -->
    <script src="~/assets/js/paper-kit.js?v=2.2.0" type="text/javascript"></script>


Add to site.js:

    <script>
      $(document).ready(function() {

        if ($("#datetimepicker").length != 0) {
          $('#datetimepicker').datetimepicker({
            icons: {
              time: "fa fa-clock-o",
              date: "fa fa-calendar",
              up: "fa fa-chevron-up",
              down: "fa fa-chevron-down",
              previous: 'fa fa-chevron-left',
              next: 'fa fa-chevron-right',
              today: 'fa fa-screenshot',
              clear: 'fa fa-trash',
              close: 'fa fa-remove'
            }
          });
        }

        function scrollToDownload() {

          if ($('.section-download').length != 0) {
            $("html, body").animate({
              scrollTop: $('.section-download').offset().top
            }, 1000);
          }
        }
      });
    </script>