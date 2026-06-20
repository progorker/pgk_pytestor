```
===========_____=======_============
  _ __ _  |_   _|__ __| |_ ___ _ _ 
 | '_ \ || || |/ -_|_-<  _/ _ \ '_|
 | .__/\_, ||_|\___/__/\__\___/_|  
=|_|===|__/=========================
 Unit testing framework for Python
====================================


-|_|-----------|___/----------------------
             Alpha Testing
------------------------------------------


-|_|-------|_|---------------------------
      Using unit testing framework
-----------------------------------------

+ Simple sample of using unit testing framework
-----
import sys
import os

sys.path.append( os.path.abspath( "../pyTestor" ) )

import pytestor

pytestor.g_testor_username = 'mytestor'
pytestor.g_testor_password = 'rzutomqahegpnyx'
pytestor.g_suite_code = 'pytestorcheck'
pytestor.g_clear_version = False
pytestor.g_last_version = 1
pytestor.g_testor_dir = '/bioogr/psk-19/pyTestor'
pytestor.g_src_dir = '/bioogr/psk-19/pyMan'
pytestor.g_case_code = 'test_numbers'

pytestor.api_testor_startup()

v_suite_id, v_case_id = pytestor.api_testor_suite_case( pytestor.g_token, pytestor.g_suite_code, pytestor.g_case_code )
print( "Suite ID: " + str(v_suite_id) + "\n" )
print( "Case ID: " + str(v_case_id) + "\n" )

v_test_code = "equals.1"
v_dbl_a = 20.5
v_dbl_b = 21.5
v_test_id = pytestor.api_testor_equals( pytestor.g_token, v_suite_id, v_case_id, v_test_code, v_dbl_a, v_dbl_b )
print( "Test ID: " + str(v_test_id) + "\n" )

func_not_declared()

pytestor.api_testor_shutdown()
-----


-|_|-------|_|---------------------------
         Getting manual page
-----------------------------------------

$) export PY_TESTOR_DIR=""
$) export MODULE="mytestor"
$) export KIND="procedure"
$) export CODE="api_testor_suite"
$) cd $PY_TESTOR_DIR && php ./man.php $MODULE $KIND $CODE

 
-|_|-------|_|---------------------------
         Getting code pattern
-----------------------------------------

$) export PY_TESTOR_DIR=""
$) export MODULE="mytestor"
$) export KIND="procedure"
$) export CODE="api_testor_suite"
$) export VARIANT="scrp"
$) cd $PY_TESTOR_DIR && php ./pattern.php $MODULE $KIND $CODE $VARIANT


-|_|-------|_|---------------------------
       Controlling source versions
-----------------------------------------

$) export PY_TESTOR_DIR=""
$) export PY_WORKED_DIR=""
$) cp -f $PY_TESTOR_DIR/csvc.php $PY_WORKED_DIR/
$) cp -f $PY_TESTOR_DIR/csvc-cfg.php $PY_WORKED_DIR/
$) nano $PY_WORKED_DIR/csvc-cfg.php
---> Modify myTestor account and other settings
$) cd $PY_WORKED_DIR && php ./csvc.php


```
