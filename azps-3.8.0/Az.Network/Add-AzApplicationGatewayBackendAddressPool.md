---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 5b41cedc02818db6c309e3c11bb1797fb6525d75
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878197"
---
# Add-AzApplicationGatewayBackendAddressPool

## SYNOPSIS
응용 프로그램 게이트웨이에 백 엔드 주소 풀을 추가 합니다.

## 구문과

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**Add-AzApplicationGatewayBackendAddressPool** cmdlet은 응용 프로그램 게이트웨이에 백 엔드 주소 풀을 추가 합니다.
백 엔드 주소는 IP 주소, FQDN (정규화 된 도메인 이름) 또는 IP 구성 Id를 사용 하 여 지정할 수 있습니다.

## 예제의

### 예제 1: 백 엔드 서버 FQDN을 사용 하 여 백 엔드 주소 풀 추가
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 Fqdn을 사용 하 여 $AppGw에 저장 된 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 추가 합니다.

### 예제 2: 백엔드 서버 IP 주소를 사용 하 여 백 엔드 주소 풀 추가
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 IP 주소를 사용 하 여 $AppGw에 저장 된 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 추가 합니다.

### 예제 3: 백엔드 서버의 IP 주소 ID를 사용 하 여 백 엔드 주소 풀 Seta
```
PS C:\>$Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 Nic01 라는 네트워크 인터페이스 개체를 가져와 $Nic 01 변수에 저장 합니다. 두 번째 명령은 ResourceGroup02 이라는 리소스 그룹에 속하는 Nic02 라는 네트워크 인터페이스 개체를 가져와 $Nic 02 변수에 저장 합니다. 세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 위의 명령은 $Nic 01 및 $Nic 02의 백 엔드 IP 구성 Id를 사용 하 여 $AppGw에 저장 된 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 추가 합니다.

## 변수

### -ApplicationGateway
이 cmdlet이 백 엔드 주소 풀을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackendFqdns
이 cmdlet이 백 엔드 서버 풀로 추가 하는 백엔드 Fqdn 목록을 지정 합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendIPAddresses
이 cmdlet이 백 엔드 서버 풀로 추가 하는 백 엔드 IP 주소 목록을 지정 합니다.

```yaml
Type: System.String[]
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
이 cmdlet이 추가 하는 백 엔드 서버 풀의 이름을 지정 합니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. * PSApplicationGateway

## 출력

### Microsoft. * PSApplicationGateway

## 상속자

## 관련 링크

[Get-AzApplicationGatewayBackendAddressPool](./Get-AzApplicationGatewayBackendAddressPool.md)

[Get-AzApplicationGatewayBackendAddressPool](./Get-AzApplicationGatewayBackendAddressPool.md)

[새로운 AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[제거-AzApplicationGatewayBackendAddressPool](./Remove-AzApplicationGatewayBackendAddressPool.md)

[Set-AzApplicationGatewayBackendAddressPool](./Set-AzApplicationGatewayBackendAddressPool.md)


