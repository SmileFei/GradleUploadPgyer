# GradleUploadPgyer


## 此内容主要针对与安卓项目中的Gradle插件脚本的多版本打包和gradle上传蒲公英

## 添加说明

build.gradle配置




    dependencies {
        classpath 'com.android.tools.build:gradle:2.1.2'
        classpath 'org.quanqi:pgyer:0.1.2'

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
	
build.gradle(app)配置



	apply plugin: 'com.android.application'
	apply plugin: 'org.quanqi.pgyer'

	.
	.
	.
	
	
	pgyer {
        _api_key = "你的蒲公英_api_key"
        uKey = "你的蒲公英uKey"
		}
	apks {
		debug {
        sourceFile = file('build/outputs/apk/app-dev-unsigned.apk')
			}
		}
		
# 用法

	$ ./gradle uploadPgyer
	





