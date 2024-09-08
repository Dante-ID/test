Test(s), testing, or TEST may refer to:

Test (assessment), an educational assessment intended to measure the respondents' knowledge or other abilities
Arts and entertainment
Test (2013 film), an American film
Test (2014 film), a Russian film
Test (group), a jazz collective
Tests (album), a 1998 album by The Microphones
Testing (album), an album by ASAP Rocky
Computing
.test, a reserved top-level domain
Software testing
test (Unix), a Unix command for evaluating conditional expressions
TEST (x86 instruction), an x86 assembly language instruction
People
Test (wrestler), ring name for Andrew Martin (1975–2009), Canadian professional wrestler
John Test (1771–1849), American politician
Zack Test (born 1989), American rugby union player
Science and technology
Experiment, a procedure carried out in order to test (support, refute, or validate) a hypothesis
Statistical hypothesis testing, techniques to reach conclusions about probabilistic behavior
Product testing
System testing
Mechanical testing
Test equipment
Stress testing
Proof test, a stress test to demonstrate the fitness of a load-bearing structure
Test (biology), the shell of sea urchins and certain microorganisms
Sports
Test cricket, a series of matches played by two national representative teams
Test match (rugby league), a match between teams of the Rugby League International Federation
Test match (rugby union), an international match usually played between two senior national teams
The Test (greyhound competition), a greyhound race run between 1941 and 2008
Other uses
River Test, a river in England
Test (law), an applied method of evaluation used to resolve matters of jurisprudence
See also

Search for "Test" on Wikipedia.
Tester (disambiguation), person or device that tests or measures
The Test (disambiguation)
All pages with titles beginning with Test
All pages with titles containing Test
Examination (disambiguation)
Trial (disambiguation)
Validation (disambiguation)
Verification (disambiguation)
This workflow uses actions that are not certified by GitHub.
# They are provided by a third-party and are governed by
# separate terms of service, privacy policy, and support
# documentation.

# This workflow will build, test, sign and package a WPF or Windows Forms desktop application
# built on .NET Core.
# To learn how to migrate your existing application to .NET Core,
# refer to https://docs.microsoft.com/en-us/dotnet/desktop-wpf/migration/convert-project-from-net-framework
#
# To configure this workflow:
#
# 1. Configure environment variables
# GitHub sets default environment variables for every workflow run.
# Replace the variables relative to your project in the "env" section below.
#
# 2. Signing
# Generate a signing certificate in the Windows Application
# Packaging Project or add an existing signing certificate to the project.
# Next, use PowerShell to encode the .pfx file using Base64 encoding
# by running the following Powershell script to generate the output string:
#
# $pfx_cert = Get-Content '.\SigningCertificate.pfx' -Encoding Byte
# [System.Convert]::ToBase64String($pfx_cert) | Out-File 'SigningCertificate_Encoded.txt'
#
# Open the output file, SigningCertificate_Encoded.txt, and copy the
# string inside. Then, add the string to the repo as a GitHub secret
# and name it "Base64_Encoded_Pfx."
# For more information on how to configure your signing certificate for
# this workflow, refer to https://github.com/microsoft/github-actions-for-desktop-apps#signing
#
# Finally, add the signing certificate password to the repo as a secret and name it "Pfx_Key".
# See "Build the Windows Application Packaging project" below to see how the secret is used.
#
# For more information on GitHub Actions, refer to https://github.com/features/actions
# For a complete CI/CD sample to get started with GitHub Action workflows for Desktop Applications,
# refer to https://github.com/microsoft/github-actions-for-desktop-apps

