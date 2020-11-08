---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217474"
---
# Get-AzDnsZone

## SYNOPSIS
DNS 영역을 가져옵니다.

## 구문과

### 기본값 (기본값)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 리소스
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (Domain Name System) 영역을 가져옵니다.
*Name* 매개 변수를 지정 하면 단일 **DnsZone** 개체가 반환 됩니다.
*Name* 매개 변수를 지정 하지 않으면 지정 된 리소스 그룹의 모든 영역이 포함 된 배열이 반환 됩니다.
**DnsZone** 개체를 사용 하 여 영역을 업데이트할 수 있습니다 (예: **레코드 집합** 개체를 추가할 수 있음).

## 예제의

### 예제 1: 영역 가져오기
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

이 예제에서는 지정 된 리소스 그룹에서 myzone.com 이라는 DNS 영역을 가져온 다음이를 $Zone 변수에 저장 합니다.

### 예제 2: 리소스 그룹의 모든 영역 가져오기
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

이 예제에서는 지정 된 리소스 그룹에 있는 모든 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.

### 예제 3: 구독에 있는 모든 영역 가져오기
```
PS C:\> $Zones = Get-AzDnsZone
```

이 예제에서는 현재 Azure 구독에 있는 모든 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -이름
가져올 DNS 영역의 이름을 지정 합니다.
*Name* 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 지정 된 리소스 그룹에 있는 모든 DNS 영역을 가져옵니다.
*ResourceGroupName* 매개 변수를 생략 해도이 cmdlet은 현재 Azure 구독에서 모든 DNS 영역을 가져옵니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가져올 DNS 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.
*ResourceGroupName* 를 지정 하지 않은 경우에는 *Name* 매개 변수도 생략 해야 합니다.
이 경우이 cmdlet은 현재 Azure 구독에서 모든 DNS 영역을 가져옵니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### DnsZone에 대 한 명령

## 상속자

## 관련 링크

[새로운 AzDnsZone](./New-AzDnsZone.md)

[제거-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
