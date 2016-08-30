It is good practice to run all unit tests before pushing code to Master. To do this, make sure the env is set using
```
source [location-of-activate-file]
```
In the root of the project, run all tests using 
```
./manage.py test
```


###SMH  1 test failure

    ....................................................................................................................................................................................................................................................................E
    ======================================================================
    ERROR: ph_operation.tests.tests_event_manager (unittest.loader.ModuleImportFailure)
    ----------------------------------------------------------------------
    ImportError: Failed to import test module: ph_operation.tests.tests_event_manager
    Traceback (most recent call last):
      File "/usr/lib/python2.7/unittest/loader.py", line 254, in _find_tests
        module = self._get_module_from_name(name)
      File "/usr/lib/python2.7/unittest/loader.py", line 232, in _get_module_from_name
        __import__(name)
      File "/home/shermes641/Desktop/PH1/ServerUI-Python/ph_operation/tests/tests_event_manager.py", line 11, in <module>
        class EventBaseTestCase(base_test.BaseTestOperation):
      File "/home/shermes641/Desktop/PH1/ServerUI-Python/ph_operation/tests/tests_event_manager.py", line 14, in EventBaseTestCase
        eventNumber=ph_model.event.EventTypeConst.GRID_FAILURE.value),
      File "/usr/local/lib/python2.7/dist-packages/django/db/models/manager.py", line 122, in manager_method
        return getattr(self.get_queryset(), name)(*args, **kwargs)
      File "/usr/local/lib/python2.7/dist-packages/django/db/models/query.py", line 387, in get
        self.model._meta.object_name
    DoesNotExist: EventType matching query does not exist.
    
    
    ----------------------------------------------------------------------
    Ran 264 tests in 89.675s
    
    FAILED (errors=1)
    Destroying test database for alias 'default'...

###SMH
