This processor is designed to do nothing and take no actions. It is intended to be used as a safe way to set variables in AutoPkg recipes where the variables aren't otherwise able to be set by other AutoPkg processors. 

For example, if you need to set the `version` output variable in an AutoPkg recipe by combining two other output variables (in this example, a `major_version` variable and a `minor_version` variable), the `VariablePlaceholder` processor can be used to do this in a safe way.

```
<dict>
   <key>Processor</key>
   <string>VariablePlaceholder</string>
   <key>Arguments</key>
   <dict>
      <key>version</key>
      <string>%major_version%.%minor_version%</string>
   </dict>
</dict>
```