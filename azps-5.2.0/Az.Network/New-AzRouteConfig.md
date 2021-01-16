---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 54a12f4485e56b592b2e42d7b9515af595d4b6c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367536"
---
# New-AzRouteConfig

## SYNOPSIS
경로 테이블에 대한 경로를 만듭니다.

## 구문

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**New-AzRouteConfig** cmdlet은 Azure 경로 테이블에 대한 경로를 만듭니다.

## 예제

### 예제 1: 경로 만들기
```powershell
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

첫 번째 명령은 Route07이라는 경로를 만든 다음, 경로 변수에 $Route 저장합니다.
이 경로는 패킷을 로컬 가상 네트워크에 전달합니다.
두 번째 명령은 경로의 속성을 표시합니다.

### 예제 2

경로 테이블에 대한 경로를 만듭니다. (자동Generated)

<!-- Aladdin Generated Example -->
```powershell
New-AzRouteConfig -AddressPrefix 10.1.0.0/16 -Name 'Route07' -NextHopIpAddress '12.0.0.5' -NextHopType 'VnetLocal'
```

## PARAMETERS

### -AddressPrefix
경로가 적용되는 대상을 CIDR(CIDR(Classless Interdomain Routing)) 형식으로 지정합니다.

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

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
경로의 이름을 지정합니다.

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

### -NextHopIpAddress
Azurevirtual 네트워크에 추가하는 가상 어플라이언스의 IP 주소를 지정합니다.
이 경로는 패킷을 해당 주소로 전달합니다.
*NextHopType* 매개 변수에 대한 VirtualAppliance 값을 지정하는 경우 이 매개 변수를 지정합니다.

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

### -NextHopType
이 경로가 패킷을 전달하는 방법을 지정합니다.
이 매개 변수에 허용되는 값은
- 인터넷.
Azure에서 제공하는 기본 인터넷 게이트웨이입니다. 
- 없음.
이 값을 지정하면 경로가 패킷을 전달하지 않습니다. 
- VirtualAppliance.
Azure 가상 네트워크에 추가하는 가상 어플라이언스입니다. 
- VirtualNetworkGateway.
Azure 서버-서버 가상 사설망 게이트웨이. 
- VnetLocal.
로컬 가상 네트워크입니다.
동일한 가상 네트워크에 10.1.0.0/16 및 10.2.0.0/16의 두 서브넷이 있는 경우 다른 서브넷으로 전달할 각 서브넷에 대한 VnetLocal 값을 선택합니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSRoute

## 참고 사항

## 관련 링크

[Add-AzRouteConfig](./Add-AzRouteConfig.md)

[Get-AzRouteConfig](./Get-AzRouteConfig.md)

[Remove-AzRouteConfig](./Remove-AzRouteConfig.md)

[Set-AzRouteConfig](./Set-AzRouteConfig.md)


