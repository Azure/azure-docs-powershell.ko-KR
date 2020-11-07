---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 67cf5adb8d8cc0bef914f0623f66ee0e871302d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875469"
---
# New-AzApplicationGatewayIPConfiguration

## SYNOPSIS
응용 프로그램 게이트웨이에 대 한 IP 구성을 만듭니다.

## 구문과

### SetByResourceId
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzApplicationGatewayIPConfiguration** cmdlet은 응용 프로그램 게이트웨이에 대 한 IP 구성을 만듭니다.
IP 구성에는 응용 프로그램 게이트웨이가 배포 되는 서브넷이 포함 됩니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이에 대 한 IP 구성을 만듭니다.
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져옵니다.

두 번째 명령은 이전 명령의 가상 네트워크가 속한 서브넷에 대 한 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.

세 번째 명령은 $Subnet를 사용 하 여 IP 구성을 만듭니다.

## 변수

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
만들려는 IP 구성의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -서브넷
서브넷 개체를 지정 합니다.
이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
서브넷 ID를 지정 합니다.
이는 응용 프로그램 게이트웨이가 배포 되는 서브넷입니다.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. *. m i m. 모델. m m m m i m a.

## 상속자

## 관련 링크

[추가-AzApplicationGatewayIPConfiguration](./Add-AzApplicationGatewayIPConfiguration.md)

[Get-AzApplicationGatewayIPConfiguration](./Get-AzApplicationGatewayIPConfiguration.md)

[제거-AzApplicationGatewayIPConfiguration](./Remove-AzApplicationGatewayIPConfiguration.md)

[Set-AzApplicationGatewayIPConfiguration](./Set-AzApplicationGatewayIPConfiguration.md)


