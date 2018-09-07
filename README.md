# rs-form-expire
A script to unpublish a form on a specific date

In RSForm Pro, there's a scripts tab, and the first box is for form out put (called "Script called on form display")

This script relies on the server time zone, so feel free to modify it to force a certain time zone. On the given date and time, the script will switch the form output to a message and hide the form.

$enddate = new DateTime('2018-11-21 23:00:00');
$now = new DateTime();

if($enddate < $now) {
    $formLayout = '<h2>Sorry, this contest has ended.</h2>';
}
