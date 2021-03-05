---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 2d79857df255bb960c51b87c536013921f3b1c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997990"
---
# Get-AzIotCentralApp

## SYNOPSIS
하나 또는 여러 IoT Central 애플리케이션에 대한 속성을 얻습니다.

## 구문

### ListIotCentralAppsParameterSet(기본값)
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
매개 변수 집합에 따라 특정 IoT Central 애플리케이션 또는 리소스 그룹 또는 구독의 모든 애플리케이션에 대한 메타데이터를 얻습니다. 

## 예제

### 예제 1 특정 IoT Central 애플리케이션을 얻습니다.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

지정된 IoT Central Application에 대한 메타데이터를 얻습니다.

출력 예제:

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXX-XXXX-XXXX-XXXX-XXX-XXXXXXXXXXXXXXXXXXXX DisplayName : 내 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXX-XXXX-XXXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName

### 예제 2 구독에서 IoT Central 애플리케이션을 얻습니다.
```powershell
PS C:\> Get-AzIotCentralApp
```

현재 구독의 모든 IoT Central 애플리케이션에 대한 메타데이터를 얻습니다.

출력 예제:

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXX-XXXX-XXXX-XXXX-XXX-XXXXXXXXXXXXXXXXXXXX DisplayName : 내 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXX-XXXX-XXXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Name : MyAppResourceName2 Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX DisplayName : My Custom 표시 이름 2 하위omain : MyAppSubdomain2 템플릿 : SubscriptionId : XXXXXX-XXXX-XXXXXXXXXXXXXXXXXXXXXXXXX 리소스 그룹 iotc-default@1.0.0 이름 : MyResourceGroupName2

### 예제 3 리소스 그룹에서 IoT Central 애플리케이션을 얻습니다.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

제공된 리소스 그룹의 모든 IoT Central 애플리케이션에 대한 메타데이터를 얻습니다.

출력 예제:

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXX-XXXX-XXXX-XXXX-XXX-XXXXXXXXXXXXXXXXXXXX DisplayName : 내 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXX-XXXX-XXXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Name : MyAppResourceName2 Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX DisplayName : My Custom 표시 이름 2 하위omain : MyAppSubdomain2 템플릿 : SubscriptionId : XXXXXX-XXXX-XXXXXXXXXXXXXXXXXXXXXXXXXX 리소스 그룹 iotc-default@1.0.0 이름 : MyResourceGroupName

## 매개 변수

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
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp

## 참고 사항

## 관련 링크
