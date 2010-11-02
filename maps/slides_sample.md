!SLIDE title-slide
.notes first slide

# First Slide #

!SLIDE bullets incremental transition=fade
.notes something something something something something something something something something something something something something something something dark side

# Second Slide #

* something
* something else
* a third thing
* a fourth thing
* a fifth thing

!SLIDE center transition=scrollUp
.notes another dark side

![octocat](octocat.png)

!SLIDE
.notes notes for my slide

	@@@ javascript
	function setupPreso() {
	  if (preso_started)
	  {
	     alert("already started")
	     return
	  }
	  preso_started = true

	  loadSlides()
	  doDebugStuff()

	  document.onkeydown = keyDown
	}

!SLIDE commandline incremental

	$ git commit -am 'incremental bullet points working'
	[master ac5fd8a] incremental bullet points working
	 2 files changed, 32 insertions(+), 5 deletions(-)

!SLIDE commandline incremental

	$ git commit -am 'incremental bullet points working'
	[bmaster ac5fd8a] incremental bullet points working
	 2 files changed, 32 insertions(+), 5 deletions(-)
	
	$ git commit -am 'incremental bullet points working'
	[cmaster ac5fd8a] incremental bullet points working
	 2 files changed, 32 insertions(+), 5 deletions(-)


!SLIDE subsection
# Custom events #

!SLIDE custom_and_unique_class
# 1st Example h1
<script>
// bind to custom event
$(".custom_and_unique_class").bind("showoff:show", function (event) {
 // animate the h1
 var h1 = $(event.target).find("h1");
 h1.delay(500)
   .slideUp(300, function () { $(this).css({textDecoration: "line-through"}); })
   .slideDown(300);
});
</script>

!SLIDE prevent_default
# 2nd Example h1
<script>
$(".prevent_default").bind("showoff:next", function (event) {
 var h1 = $(event.target).find("h1");
 if (h1.css("text-decoration") === "none") {
   event.preventDefault();
   h1.css({textDecoration: "line-through"})
 }
});
</script>

!SLIDE
# Switched #


!SLIDE subsection

# Subsection Slide #

!SLIDE

# Code Slide #

	@@@ ruby
	require 'sinatra/base'

	class MyApp < Sinatra::Base
	  set :sessions, true
	  set :foo, 'bar'

	  get '/' do
	    'Hello world!'
	  end
	end	

!SLIDE execute

# Executable JavaScript #

	@@@ javaScript
	result = 3 + 3;

!SLIDE

# Write your own slides #

## Using [markdown](http://daringfireball.net/projects/markdown/)

    !SLIDE
    
    # Title of the slide #
    
    How easy is this?

