## Overview
Laravel stubs are helper modules that enable us to customize the default Artisan generated classes.

For example, when you need to send data to a database, you are supposed to indicate fields that are ＄fillable or ＄guarded. This can be very time-consuming when it comes to creating an Enterprise system that involves hundreds of tables, as you will need to make these changes for each and every model.

With stubs, you can simply indicate that you want all models to have ＄guarded = []. This should be done before you start creating the models.

Example
Let’s go over an example. First, we have to publish the stubs.

Run the command below:

# php artisan stub:publish
You will notice a new stubs directory. In the stubs directory, there are files that can also be used for customization, as discussed above. For this shot, we will be editing the model.stub file.

widget

# Let’s now add ＄guarded=[] to the model stub:

``` 
 <?php

 namespace {{ namespace }};

 use Illuminate\Database\Eloquent\Model;

 class {{ class }} extends Model
 {
    // let us make customize it
 protected ＄guarded = [];

}

``` 

Now that we have added the ＄guarded=[] property to the stub for the model, we run the command to create a new TestStubModel:

php artisan:make:model TestStubModel
widget
You will notice that the code above has protected ＄guarded=[];, and any other model you create will come with this property.

## Summary
Laravel stubs enable easy customization of created class properties, which increases the speed of developers.
