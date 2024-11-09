from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()

# add ds18b20 src files.
if GetDepend('PKG_DS18B20_USING_SENSOR_V1'):
    src += ['src/dallas_ds18b20_sensor_v1.c']

if GetDepend('PKG_DS18B20_USING_SAMPLE_SENSOR_V1'):
    src += Glob('sample/ds18b20_sample.c')



# add ds18b20 include path.
path  = [cwd + '/inc']

# add src and include to group.
group = DefineGroup('ds18b20', src, depend = ['PKG_USING_DS18B20'], CPPPATH = path)

Return('group')