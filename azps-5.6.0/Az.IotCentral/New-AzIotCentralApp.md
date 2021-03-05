---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: ffae73880f66e378c7270ba5ce3645eae63064ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997985"
---
# New-AzIotCentralApp

## SYNOPSIS
새 IoT Central Application을 만듭니다.

## 구문

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
제공된 속성 및 메타데이터를 사용하여 새 IoT Central Application을 만듭니다. IoT Central에 대한 소개는 https://docs.microsoft.com/azure/iot-central/ 를 참조합니다.

## 예제

### 예제 1 간단한 IoT Central Application 만들기.
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

출력 예제:

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXX-XXX-XXX-XXus XXXXXXXXXXXXXXXXXXXXXXXXXXXX 리소스GroupName : MyAppResourceName Subdomain : MyAppSubdomain 템플릿 : SubscriptionId : XXXXXXXX-XXXX-XXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName

리소스 그룹의 지역에 있는 표준 가격 책정 계층 ST2에서 IoT Central 애플리케이션을 생성합니다.

### 예제 2 간단한 IoT Central Application 만들기
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

출력 예제:

ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXX-XXX-XXXX-XXX-X XXXX-XXXXXXXXXXXXXXXXX 디스플레이 이름 : 내 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : SubscriptionId : XXXXXXX-XXXXX-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName

iotc-default 템플릿을 기반으로 사용자 지정 표시 이름으로 'westus' 지역에서 표준 가격 책정 계층 ST2를 사용하여 IoT Central 애플리케이션을 만듭니다.

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
IoT Central 애플리케이션에 대한 사용자 지정 표시 이름입니다.
기본값은 리소스 이름입니다.

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

### -Location
IoT Central 애플리케이션의 위치입니다.
기본값은 대상 리소스 그룹의 위치입니다.

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

### -Name
Iot Central Application Resource의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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
IoT Central URL에 대한 하위omain입니다.
각 애플리케이션에는 고유한 하위omain이 있어야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Template
IoT Central 애플리케이션 템플릿 이름입니다.
기본값은 사용자 지정 애플리케이션입니다.

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

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp

## 참고 사항

## 관련 링크
