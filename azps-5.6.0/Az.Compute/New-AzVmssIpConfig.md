---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 30dbe52805017a00f24cc95c832386545ae036e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965040"
---
# New-AzVmssIpConfig

## SYNOPSIS
VMSS의 네트워크 인터페이스에 대한 IP 구성을 만듭니다.

## 구문

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**New-AzVmssIpConfig** cmdlet은 VMSS(Virtual Machine Scale Set)의 네트워크 인터페이스에 대한 IP 구성 개체를 만듭니다.
이 cmdlet에서 구성을 Add-AzVmssNetworkInterfaceConfiguration *ipConfiguration* 매개 변수로 지정합니다.

## 예제

### 예제 1: VMSS 인터페이스에 대한 IP 구성 개체 만들기
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

이 명령은 ContosoVmssInterface02라는 IP 구성 개체를 만듭니다.
명령은 이전에 정의된 서브넷 ID를 $SubnetId.
명령은 **Add-AzVmssNetworkInterfaceConfiguration** 에서 나중에 사용할 $IPConfiguration 변수에 구성 설정을 저장합니다.

### 예제 2: NAT 풀 설정을 포함하는 IP 구성 개체 만들기
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

이 명령은 ContosoVmssInterface03이라는 IP 구성 개체를 만든 다음 나중에 사용할 $IPConfiguration 변수에 저장합니다.
명령은 이전에 정의된 서브넷 ID를 $SubnetId.
명령은 나중에 사용할 $IPConfiguration 변수에 구성 설정을 저장합니다.
명령은 *LoadBalancerInboundNatPoolsId* 및 *LoadBalancerBackendAddressPoolsId* 매개 변수에 대한 값을 지정합니다.

## 매개 변수

### -ApplicationGatewayBackendAddressPoolsId
부하 저울의 백END 주소 풀에 대한 참조 배열을 지정합니다.
확장 집합은 하나의 공용 및 하나의 내부 부하 균형 조정기의 백던드 주소 풀을 참조할 수 있습니다.
여러 확장 집합은 동일한 부하 저울을 사용할 수 없습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DnsSetting
publicIP 주소에 적용할 dns 설정입니다.
공용IP 주소에 적용할 Dns 설정의 도메인 이름 레이블입니다.
도메인 이름 레이블 및 vm 인덱스의 연결은 만들 공용 IP 주소 리소스의 도메인 이름 레이블이 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
IP 태그 개체의 배열을 지정합니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
부하 저울의 들어오는 NAT(네트워크 주소 변환) 풀에 대한 참조 배열을 지정합니다.
확장 집합은 하나의 공용 및 하나의 내부 부하 균형 조정기에서 들어오는 NAT 풀을 참조할 수 있습니다.
여러 확장 집합은 동일한 부하 저울을 사용할 수 없습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
부하 저울의 들어오는 NAT 풀에 대한 참조 배열을 지정합니다.
확장 집합은 하나의 공용 및 하나의 내부 부하 균형 조정기에서 들어오는 NAT 풀을 참조할 수 있습니다.
여러 확장 집합은 동일한 부하 저울을 사용할 수 없습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
IP 구성의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Primary
네트워크 인터페이스에 IP 구성이 두 개 이상 있는 경우 기본 IP 구성을 지정합니다.

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

### -PrivateIPAddressVersion
개인 IP 주소에 대한 IP 구성을 지정합니다.  기본값은 IPv4로 사용됩니다.  가능한 값은 'IPv4' 및 'IPv6'입니다.

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

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
공용 IP 주소의 유휴 시간 제한입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
publicIP 주소 구성 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
공용 IP 주소에 대한 IP 구성을 지정합니다.  기본값은 IPv4로 사용됩니다.  가능한 값은 'IPv4' 및 'IPv6'입니다.

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

### -PublicIPPrefix
공용 IP 연결선의 ID

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

### -SubnetId
구성에서 VMSS 네트워크 인터페이스를 만드는 서브넷 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다. cmdlet이 실행되지 않습니다.

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

### System.String[]

### System.Int32

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]

## 출력

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration

## 참고 사항

## 관련 링크

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


