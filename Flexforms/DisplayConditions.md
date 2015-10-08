```xml
<T3DataStructure>
    <meta>
        <langDisable>1</langDisable>
    </meta>
    <sheets>
        <sDEF>
            <ROOT>
                <TCEforms>
                    <sheetTitle>Switch</sheetTitle>
                </TCEforms>
                <type>array</type>
                <el>
                    <myAwesomeSwitch>
                        <TCEforms>
                            <label>Switch</label>
                            <onChange>reload</onChange>
                            <config>
                                <type>select</type>
                                <items>
                                    <numIndex index="0">
                                        <numIndex index="0">a</numIndex>
                                        <numIndex index="1">10</numIndex>
                                    </numIndex>
                                    <numIndex index="1">
                                        <numIndex index="0">b</numIndex>
                                        <numIndex index="1">20</numIndex>
                                    </numIndex>
                                </items>
                            </config>
                        </TCEforms>
                    </myAwesomeSwitch>
                    
                    <myCondition>
                        <TCEforms>
                            <label>Something Else</label>
                            <displayCond>FIELD:myAwesomeSwitch:=:20</displayCond>
                            <config>
                                ...
                            </config>
                        </TCEforms>
                    </myCondition>
                </el>
            </ROOT>
        </sDEF>
    </sheets>
</T3DataStructure>
```