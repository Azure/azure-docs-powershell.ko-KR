---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: f99faf1ce7420212e87c894c8f5aadeb16578334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997962"
---
# Set-AzIotCentralApp

## SYNOPSIS
IoT Central Application에 대한 메타데이터를 업데이트합니다.

## 구문

### ResourceIdParameterSet(기본값)
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectParameterSet
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
IoT Central Application의 메타데이터를 업데이트합니다. 

## 예제

### 예제 1 표시 이름 업데이트
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

기존 IoT Central 애플리케이션에서 표시 이름을 업데이트합니다.

출력 예제:

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXX-XXX-XXXX-XXX-X XXXXXXXXXXXXXXXXXXXXXXX 디스플레이 이름 : MyAppSubdomain 템플릿 : SubscriptionId : XXXXXXXX-XXXX-XXXXXXXXXXXXXXXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName

### 예제 2 하위마인 업데이트
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

기존 IoT Central 애플리케이션에서 표시 이름을 업데이트합니다.

출력 예제:

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXXXXXXXX 디스플레이 이름 : 표시 이름 하위omain : new-subdomain 템플릿 : SubscriptionId : XXXXXXX-XXXX-XXXXX-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName

### 예제 3 앱 Sku 정보 업데이트
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

기존 IoT Central 애플리케이션에서 sku를 업데이트합니다.

출력 예제:

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXXX-XXXX-XXX-XXXX-XXXX-XXXXXXXXXXXXXXXXXX 디스플레이 이름 : 표시 이름 하위omain : MyAppSubdomain 템플릿 : SubscriptionId : XXXXXXX-XXXX-XXXXX-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName

## 매개 변수

### -AsJob
백그라운드에서 작업으로 cmdlet을 실행합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Iot Central 애플리케이션의 사용자 지정 표시 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Iot Central 애플리케이션 입력 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Iot Central Application Resource의 이름입니다.

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Iot Central 애플리케이션 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
IoT Central 애플리케이션에 대한 가격 책정 계층입니다.
기본값은 ST2입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subdomain
IoT Central Application의 하위종입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Iot Central 애플리케이션 리소스 태그입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp

## 출력

### Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp

## 참고 사항

## 관련 링크
