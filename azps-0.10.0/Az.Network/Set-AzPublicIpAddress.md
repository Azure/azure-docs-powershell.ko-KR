---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876556"
---
# Set-AzPublicIpAddress

## SYNOPSIS
공용 IP 주소에 대 한 목표 상태를 설정 합니다.

## 구문과

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzPublicIpAddress** cmdlet은 공용 IP 주소에 대 한 목표 상태를 설정 합니다.

## 예제의

### 1: 공용 IP 주소의 배정 방법 변경
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 첫 번째 명령은 리소스 그룹 $rgName에서 이름이 $publicIPName 인 공용 IP 주소 리소스를 가져옵니다.
두 번째 명령은 공용 IP 주소 개체의 배정 방법을 "Static"으로 설정 합니다.
Set-AzPublicIPAddress 명령은 업데이트 된 개체로 공용 IP 주소 리소스를 업데이트 하 고 할당 메서드를 ' Static '으로 수정 합니다. 공용 IP 주소가 즉시 할당 됩니다.

### 2: 공용 IP 주소의 DNS 도메인 레이블 변경
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

첫 번째 명령은 리소스 그룹 $rgName에서 이름이 $publicIPName 인 공용 IP 주소 리소스를 가져옵니다.
두 번째 명령은 DomainNameLabel 속성을 필수 dns 접두사로 설정 합니다.
Set-AzPublicIPAddress 명령은 공용 IP 주소 리소스를 업데이트 된 개체로 업데이트 합니다. DomainNameLabel & Fqdn이 예상 대로 수정 됩니다.

## 변수

### -AsJob
백그라운드에서 cmdlet 실행

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -PublicIpAddress
공용 IP 주소를 설정 해야 하는 목표 상태를 나타내는 **PublicIpAddress** 개체를 지정 합니다.

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSPublicIpAddress
' PublicIpAddress ' 매개 변수는 파이프라인에서 ' PSPublicIpAddress ' 형식의 값을 허용 합니다.

## 출력

### PSPublicIpAddress에 대 한.

## 상속자

## 관련 링크

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[새로운 AzPublicIpAddress](./New-AzPublicIpAddress.md)

[제거-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


