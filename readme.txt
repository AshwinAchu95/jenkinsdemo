buildscript {
	repositories {
		mavenCentral()
		maven {
			url "https://plugins.gradle.org/m2/"
		}
	}
	dependencies {
		classpath "org.sonarsource.scanner.gradle:sonarqube-gradle-plugin:2.7.1"
		classpath("org.springframework.boot:spring-boot-gradle-plugin:2.1.4.RELEASE")
	}

}

plugins {
	id 'org.springframework.boot' version '2.2.6.RELEASE'
	id 'io.spring.dependency-management' version '1.0.8.RELEASE'
	id 'java'
	id 'org.sonarqube' version '2.8'
}
group = 'com.example.tech'
version = '1.0'
sourceCompatibility = '11'

repositories {
	mavenCentral()
}

dependencies {
	implementation 'org.springframework.boot:spring-boot-starter'
	testImplementation 'org.springframework.boot:spring-boot-starter-test'

}

test {
	useJUnitPlatform()
}

