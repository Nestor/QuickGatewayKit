# QuickGatewayKit

QuickGatewayKit

  1.  Preamble

        QuickGatewayKit was produced in most part with Initializr.
        Many thanks and praise for http://www.initializr.com/ and Jonathan Verrecchia!!
        Many thanks and praise to the twbs/bootstrap team!!
        
        This web-kit is offered AS IS and WITHOUT WARRANTY.
        This web-kit is released under Creative Commons.  See http://www.quickgatewaykit.org
        and refer to the demo site's footer for more details about this license.
        
        QuickGatewayKit was first authored on May 11, 2015 by Taylor Warden.
        
        QGK was created for interested developers to begin a Ripple-based business. 
        QGK is being created with modularity in mind, so each step of development will
        not only further the long-term development roadmap, but allow developers different
        options through the variety of features which will be implemented with each version 
        this web-kit releases.  QGK is being created for developers of services for the Ripple
        protocol in mind, however, a secondary focus is this web-kit should be easily modified
        to allow for a Cryptocurrency Exchange to be created, with QGK being used as a resource
        for getting started.  The development team has chosen the HTML5coin wallet software as 
        the  asset for the default deposit and withdrawal actions.  The reason or this decision
        is that any source code forked from Bitcoin or Litecoin's code should include the same
        or very similar processes for the scripts this web-kit provides to allow for a resource
        as how to implment cryptocurrency deposits and withdrawals.
        
        Please do your own due diligence when developing a Ripple business, such as 
        a Gateway.  You must do your own research and contact relevent Government
        regulatory bodies within your country in writing with the final version of 
        your Terms of Service before you conduct any business.
        
        It is VERY much suggested that before you continue any further to consult all of
        the Ripple Whitepapers found @ https://forum.ripple.com/viewtopic.php?t=4301
        
        I, TAYLOR WARDEN, HEREBY CLAIM NO RESPONSIBILITY THEREIN FOR ANY INDIVIDUAL, 
        INDIVIDUALS, ENTITY, OR ENTITIES THAT MAY RECEIVE LEGAL ACTION, DIRECTLY OR INDIRECTLY,
        FOR THE USAGE OF THIS OR ANY PORTION OF THESE DOCUMENTS, IN PART OR IN FULL.  
        IN THE CASE OF A CIVIL LAWSUIT BEING ISSUED REGARDING THE USAGE OF THESE MATERIALS,
        THE RESULTING LAWSUIT WILL BE HEARD FROM WITHIN A COURT OF ONTARIO, CANADA.
        
        2. TABLE OF CONTENTS
        
        1.  Preamble
        2.  Table of Contents
        3.  Getting Started
        4.  Editing the Front-end
        5.  Editing the Back-end
        6.  You now have a Mock Gateway!  
        7.  Donations
        8.  Join the Ripple Community
        
        The contents of this web-kit include the following:
        
        index.php:  It is the home page of your Gateway website.  The default 
        deposit action is linked to this page via deposit.php
        
        tpl.php:  this is your template file that you can copy, rename, and 
        edit for a new page.
        
        tos.php:  this is an extremely basic Terms of Service template.  You 
        ABSOLUTELY MUST have registered a LEGAL BUSINESS within your legal 
        jurisidiction BEFORE YOU CONDUCT BUSINESS as a Ripple Gateway.  
        If you have problems with writing your terms, hire a lawyer or 
        consult twarden on the Official Ripple forums for the possibility of
	consulting or further resources.
        
        irba.php:  The International Ripple Business Association (IRBA) is 
        an organization in which member Gateways must abide by a strict 
        business practices and disclosure agreements.  The IRBA verifies 
        important information such as banking information.  This page includes
        more information on the IRBA an a simple template.  It is highly suggested
        if you are serious about operating a Gateway to one day apply for membership.
        This page becomes more important as your Gateway project becomes more established.
        
        deposit.php:  the script that processes the asset offered by default on index.php.
        
        withdrawals.php:  the page to fill out a form to process a withdrawal notification 
        via withdraw.php.
        
        xdeposit.php:  the page for a dedicated deposit form for a second option.  
        Processed via xd.php
        
        xwithdraw.php:  the page for a dedicated withdrawal form for a second option.  
        Processed via xw.php
        
        ydeposit.php:  the page for a dedicated deposit form for a second option.  
        Processed via xd.php
        
        ywithdraw.php:  the page for a dedicated withdrawal form for a second option.  
        Processed via xw.php
        
        3.  Getting Started
        
        By now, you should have read the Ripple Whitepapers, know of how legal it 
        is to operate a Gateway in your legal jurisdictionn, and have an idea of
        what you would like to offer to the Ripple network.
        
	If your server is a freshly installed Ubuntu 14.04 LTS deployment, perform the following tasks
	as root or as a user with sudo access.  QGK is tested on this distro and Debian 8.1 Jessie.

	Copy and paste into the following sources.list file these respositories:

	deb http://download.webmin.com/download/repository sarge contrib 
	
	deb http://webmin.mirror.somersettechsolutions.co.uk/repository sarge contrib

	Run sudo nano /etc/apt/sources.list, navigate to the bottom of the document
	and paste the repository URLs at the bottom of the file.  Commit changes and exit.

	Navigate to the QGK directory and run sh setup.sh.  This will update your system and install
	software packages this webkit and your web server will require to operate.  
	
	Now run mysql_setup.sh by entering sh mysql_setup.sh qgk qgk_user PASSWORD 
	
	where PASSWORD is a secure password for this database user.

        Next, open index.php.  Read the document entirely an replace the lorem ipsum text with
        your business information.  When editing the form on this page, change XXXamount
        and XXX Amount to the default asset ticket for your Gateway.
        
        4.  Editing the Front-end
        
        When you have figured out your service fees for the IOUs your Gateway issues, edit the 
        remaining pages: xdeposit.php, ydeposit.php xwithdraw.php, and ywithdraw.php.
        
        Once you have completed that, you are nearly half way there.  Now, you must
        complete your Terms of Service.  A template to get you started is found within
        tos.php.
        
        A include file is, include.php, will replicate information such as the Gateway's name, operator's name,
        as well as allow for you to manage accepted assets and their estimated delivery times.
        
        5.  Editing the Back-end
        
        xd.php, xw.php, yd.php, yw.php, deposit.php, and withdraw.php are all back-end
        PHP scripts which process a deposit notification for the Gateway operator to process.
       
        Replace XXXamount and XXX amount with the proper asset codes.
        
        Index.php links to deposit.php
        Withdrawals.php links to withdraw.php
        xdeposit.php links to xd.php
        xwithdraw.php links to xw.php
        ydeposit.php links to yd.php
        ywithdraw.php links to yw.php
        
        6.  You now have a Mock Gateway!  
        
        Now is the time to advertise your site and start market making over Ripple.
        The last step is to edit irba.php with the required information as outlined 
        by ripplebusiness.org before applying for membership.
        
        7.  Donations
        
        Please consider donating a small amount of XRP or Bitcoin to:
        https://www.bountysource.com/teams/qgk
        
        for the continued development of this web-kit if this resource 
        was helpful for starting your Ripple-based or Cryptocurrency Exchange business.
       
       8.  Join the Ripple Community!
       
       Join us at the official Ripple forums!  https://forum.ripple.com/
