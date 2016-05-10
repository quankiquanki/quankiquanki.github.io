---
layout: page
title: Contact
---

If you have questions, projects or tasks that you need my help with. Feel free to contact me through the form. I will try to get back to you as fast as I can.

<form role="form" method="POST" action="https://formspree.io/quankiquanki@gmail.com">
	<input type="hidden" name="_subject" value="Message submitted through quangn.com" />
	<div class="form-group">
		<label for="name" class="col-sm-2 control-label">Name</label>
		<div class="col-sm-10">
			<input type="text" class="form-control" id="name" name="name" placeholder="First and Last Name" value="" required="true">
		</div>
	</div>	
	<div class="form-group">
		<label for="email" class="col-sm-2 control-label">Email</label>
		<div class="col-sm-10">
			<input type="email" class="form-control" id="email" name="_replyto" placeholder="example@domain.com" value="" required="true">
		</div>
	</div>
	<div class="form-group">
		<label for="message" class="col-sm-2 control-label">Message</label>
		<div class="col-sm-10">
			<textarea class="form-control" rows="8" name="body" required="true"></textarea>
		</div>
	</div>
	<div class="form-group">
		<div class="col-sm-10 col-sm-offset-2">
			<input id="submit" name="submit" type="submit" value="Send" class="btn btn-success">
		</div>
	</div>
	<input type="hidden" name="_next" value="{{site.baseurl}}/contact/success.html" />	
</form>