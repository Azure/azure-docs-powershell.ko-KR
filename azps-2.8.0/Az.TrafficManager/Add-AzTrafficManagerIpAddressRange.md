---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 184b949fa91c7c9993895c8150e21f56244f6e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872950"
---
# Add-AzTrafficManagerIpAddressRange

## SYNOPSIS
로컬 트래픽 관리자 끝점 개체에 주소 범위 또는 서브넷을 추가 합니다.

## 구문과

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzTrafficManagerIpAddressRange** cmdlet은 로컬 Azure 트래픽 관리자 끝점 개체에 IP 주소 범위를 추가 합니다.
New-AzTrafficManagerEndpoint 또는 Get-AzTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 가져올 수 있습니다.

이 cmdlet은 로컬 끝점 개체에서 작동 합니다.
Set-AzTrafficManagerEndpoint cmdlet을 사용 하 여 트래픽 관리자의 끝점에 대 한 변경 내용을 커밋합니다.

## 예제의

### 예제 1: 끝점에 IP 주소 범위 추가
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

첫 번째 명령은 **New AzTrafficManagerEndpoint** cmdlet을 사용 하 여 Azure Traffic Manager 끝점을 만듭니다.
명령은 로컬 끝점을 $TrafficManagerEndpoint 변수에 저장 합니다.
두 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에 대 한 IP 주소 범위 1.2.3.4를 5.6.7.8에 추가 합니다.
세 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에 9.10.11.255 IP 주소 범위 9.10.11.0를 추가 합니다.
네 번째 명령은 범위가 범위 크기와 일치 하는지 확인 한 다음 $TrafficManagerEndpoint에 저장 된 끝점에 대 한 IP 주소 범위 12.13.14.0를 12.13.14.31에 추가 합니다.
다섯 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에 15.16.17.18 IP 주소 범위 15.16.17.18를 추가 합니다.
마지막 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -마지막
추가할 범위의 마지막 IP 주소를 지정 합니다.

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

### -범위
추가할 IP 주소 범위의 범위를 지정 합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.
이 cmdlet은이 로컬 개체를 수정 합니다.
**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzTrafficManagerEndpoint 또는 New-AzTrafficManagerEndpoint cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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

### -첫 번째
추가할 범위의 첫 번째 IP 주소를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### TrafficManager. TrafficManagerEndpoint/.

## 출력

### TrafficManager. TrafficManagerEndpoint/.

## 상속자

## 관련 링크

[제거-AzTrafficManagerIpAddressRange](./Remove-AzTrafficManagerIpAddressRange.md)

[새로운 AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
