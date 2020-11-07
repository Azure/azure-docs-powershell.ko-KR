---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 026e9a5bcad55312156be4a14eea238c063b9caa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703358"
---
# Add-AzureRmLoadBalancerFrontendIpConfig

## SYNOPSIS
부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### SetByResourceSubnet
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceIdSubnet
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceIdPublicIpAddress
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourcePublicIpAddress
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Add-AzureRmLoadBalancerFrontendIpConifg** Cmdlet은 Azure 부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.

## 예제의

### 예제 1 동적 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

첫 번째 명령은 MyVnet 이라는 Azure 가상 네트워크를 가져오고 파이프라인을 사용 하 여 **AzureRmVirtualNetworkSubnetConfig** cmdlet에 대 한 결과를 전달 하 여 myvnet 이라는 서브넷을 가져옵니다.
그런 다음 명령을 $Subnet 이라는 변수에 결과를 저장 합니다.
두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 **AzureRmLoadBalancerFrontendIpConfig** cmdlet에 전달 하며,이는 $MySubnet 이라는 변수에 저장 된 서브넷의 동적 개인 ip 주소를 사용 하 여 로드 균형 조정기에 프런트 엔드 ip 구성을 추가 합니다.

### 예제 2 고정 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

첫 번째 명령은 MyVnet 이라는 Azure 가상 네트워크를 가져오고 파이프라인을 사용 하 여 **AzureRmVirtualNetworkSubnetConfig** cmdlet에 대 한 결과를 전달 하 여 myvnet 이라는 서브넷을 가져옵니다.
그런 다음 명령을 $Subnet 이라는 변수에 결과를 저장 합니다.
두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 **AzureRmLoadBalancerFrontendIpConfig** cmdlet에 전달 하며,이는 $Subnet 이라는 변수에 저장 된 서브넷의 고정 개인 ip 주소를 사용 하 여 로드 균형 조정기에 프런트 엔드 ip 구성을 추가 하는 것을 반환 합니다.

### 예제 3 공용 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

첫 번째 명령은 MyPub 이라는 Azure 공개 IP 주소를 가져온 다음 그 결과를 $PublicIp 이라는 변수에 저장 합니다.
두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 AzureRmLoadBalancerFrontendIpConfig cmdlet에 전달 하 고 공용 IP 주소가 $PublicIp 라는 변수에 저장 된 부하 분산에 프런트 엔드 IP 구성을 추가 하는 결과를 **추가** 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancer
**LoadBalancer** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
추가할 프런트 엔드 IP 구성의 이름을 지정 합니다.

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

### -PrivateIpAddress
프런트 엔드 IP 구성에 연결할 개인 IP 주소를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
프런트 엔드 IP 구성과 연결할 공용 IP 주소를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressId
프런트 엔드 IP 구성을 추가할 공용 IP 주소의 ID를 만듭니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -서브넷
프런트 엔드 IP 구성을 추가할 서브넷 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
프런트 엔드 IP 구성을 추가할 서브넷의 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSLoadBalancer
' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. 네트워크. PSLoadBalancer

## 상속자

## 관련 링크

[Get-AzureRmLoadBalancerFrontendIpConfig](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)

[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[새로운 AzureRmLoadBalancerFrontendIpConfig](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[제거-AzureRmLoadBalancerFrontendIpConfig](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[Set-AzureRmLoadBalancerFrontendIpConfig](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


