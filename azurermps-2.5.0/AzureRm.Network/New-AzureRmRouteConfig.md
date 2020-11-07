---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: ab528e837f6f2e45db5e68430d973e0d8f019850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882610"
---
# New-AzureRmRouteConfig

## SYNOPSIS
경로 테이블에 대 한 경로를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmRouteConfig** Cmdlet은 Azure 경로 테이블에 대 한 경로를 만듭니다.

## 예제의

### 예제 1: 경로 만들기
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

첫 번째 명령은 Route07 이라는 경로를 만든 다음이를 $Route 변수에 저장 합니다.
이 경로는 패킷을 로컬 가상 네트워크에 전달 합니다.

두 번째 명령은 경로의 속성을 표시 합니다.

## 변수

### -AddressPrefix
경로가 적용 되는 대상을 클래스를 도메인간 라우팅 (CIDR) 형식으로 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
경로의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NextHopIpAddress
Azurevirtual 네트워크에 추가 하는 가상 기기의 IP 주소를 지정 합니다.
이 경로는 패킷을 해당 주소로 전달 합니다.
*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextHopType
이 경로에서 패킷을 전달 하는 방법을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 인터넷.
Azure에서 제공 하는 기본 인터넷 게이트웨이입니다. 
- 않아야.
이 값을 지정 하는 경우 경로는 패킷을 전달 하지 않습니다. 
- VirtualAppliance.
Azure 가상 네트워크에 추가 하는 가상 어플라이언스 
- VirtualNetworkGateway.
Azure 서버 간 가상 개인 네트워크 게이트웨이. 
- VnetLocal.
로컬 가상 네트워크.
동일한 가상 네트워크에 두 개의 서브넷, 10.1.0.0/16, 10.2.0.0/16이 있는 경우 각 서브넷에 대 한 VnetLocal 값을 선택 하 여 다른 서브넷으로 전달 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### Microsoft. 네트워크 모델. PSRoute

## 상속자

## 관련 링크

[추가-AzureRmRouteConfig](./Add-AzureRmRouteConfig.md)

[Get-AzureRmRouteConfig](./Get-AzureRmRouteConfig.md)

[제거-AzureRmRouteConfig](./Remove-AzureRmRouteConfig.md)

[Set-AzureRmRouteConfig](./Set-AzureRmRouteConfig.md)


