@echo off
cd /d "%~dp0"

echo.
echo Deleting pack01 to pack66...
echo.

for /L %%i in (1,1,66) do (
    set "num=0%%i"
    call set "folder=pack%%num:~-2%%"
    call if exist "%%folder%%" rmdir /s /q "%%folder%%"
)

echo.
echo =====================================
echo pack01 to pack66 deleted successfully!
echo =====================================
echo.
pause