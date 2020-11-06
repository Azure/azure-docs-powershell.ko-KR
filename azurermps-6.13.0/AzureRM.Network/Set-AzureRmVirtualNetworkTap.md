---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536552"
---
# Set-AzureRmVirtualNetworkTap

## SYNOPSIS
가상 네트워크에 대 한 목표 상태를 설정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmVirtualNetworkTap** 는 Azure 가상 네트워크를 탭 하는 데 필요한 목표 상태를 설정 합니다.

## 예제의

### 예제 1: 가상 네트워크 구성 탭
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

명령이 대상 IpConfiguration을 업데이트 하 고 가상 네트워크 탭을 업데이트 합니다.
이를 참조 하는 탭 구성이 있으면 모든 원본 트래픽이 새 대상 ip 구성 사후 업데이트로 미러링 되지 않습니다.

## 변수

### -AsJob
백그라운드에서 cmdlet 실행

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

### -VirtualNetworkTap
가상 네트워크 탭

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSVirtualNetworkTap에 대 한.

## 출력

### PSVirtualNetworkTap에 대 한.

## 상속자

## 관련 링크
