# Monarch Hotel Booking Widget Instructions

## Step 1:
Upload [`daterangepicker.min.css`](https://raw.githubusercontent.com/mrpunkin/monarch-widget/master/daterangepicker.min.css), [`jquery.monarch-booking.css`](https://raw.githubusercontent.com/mrpunkin/monarch-widget/master/jquery.monarch-booking.css) and [`jquery.monarch-booking.js`](https://raw.githubusercontent.com/mrpunkin/monarch-widget/master/jquery.monarch-booking.js) to the same publicly accessible directory on the server

## Step 2:
Place these lines in the `<head>` of any pages that will have the booking form, or all pages if you want as it will only run if there is a form. You will need to replace the `/path/to` portion of the paths with the appropriate path to the actual files.

If placing in the `<head>` is not possible, you can place just before the form HTML instead.

    <link type="text/css" rel="stylesheet" href="/path/to/jquery.monarch-booking.css" />
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script src="/path/to/jquery.monarch-booking.js"></script>


## Step 3:
Place the following form HTML anywhere you want the booking form to show.

Append the class `long` for the wider version of the form.

    <form action="https://gc.synxis.com/rez.aspx" class="bookingForm">
      <div class="bookingCalendar"></div>
      <strong class="bookingLegend">Book Your Room</strong>
      <fieldset>
        <label for="bookingRange" class="bookingFieldWrap">
          <input class="bookingField" type="text" name="range" readonly value="3/18/2018 - 3/24/2018" aria-label="Date Range" />
          <i class="material-icons">date_range</i>
        </label>
        <input type="hidden" name="arrive" />
        <input type="hidden" name="depart" />

        <label for="adult" class="bookingFieldWrap">
          <select class="bookingField" name="adult" aria-label="Adults">
            <option value="1">1 Adult</option>
            <option value="2">2 Adults</option>
            <option value="3">3 Adults</option>
            <option value="4">4 Adults</option>
          </select>
          <i class="material-icons">keyboard_arrow_down</i>
        </label>

        <label for="child" class="bookingFieldWrap">
          <select class="bookingField" name="child" aria-label="Children">
            <option value="0">0 Children</option>
            <option value="1">1 Child</option>
            <option value="2">2 Children</option>
            <option value="3">3 Children</option>
          </select>
          <i class="material-icons">keyboard_arrow_down</i>
        </label>

        <input class="bookingSubmit" type="submit" value="Book Now" role="button" />
        <input type="hidden" name="Hotel" value="78317" />
        <input type="hidden" name="Chain" value="17448" />
        <input type="hidden" name="template" value="RBE" />
        <input type="hidden" name="shell" value="RBE" />
      </fieldset>
      <a href="tel:1-800-492-8700" class="bookingSub phone" role="link" aria-label="Call to Book">1-800-492-8700</a>
    </form>
