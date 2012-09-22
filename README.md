PHP Singleton Trait
===================

A quick way to turn any class into a singleton using this trait.

## Usage
You can easily turn your classes into singletons. See the following example.

	<?php
	class MySingletonClass
	{
		use Singleton;
		
		public function init()
		{
			// Your __construct code goes here
		}

		public static function helloWorld()
		{
			// You create your class normally from now on
			// but using self::instance() instead of $this.
			// You can also return self::instance() and 
			// chain your methods.

			echo 'Hello World';
			
			return self::instance();
		}

		public static function helloAgain()
		{
			echo '<br>Hello again';
		}
	}

You can then call any of these functions statically and method chain them as if they were instantiated.

	MySingletonClass::helloWorld()->helloAgain();

This would output:

	Hello World
	Hello again

If you would like to submit changes or pull requests then please feel free.