---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 5936a7e3f15919e00fa052a2950fd31e69ca32fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875564"
---
# Get-AzNetworkInterfaceIpConfig

## SYNOPSIS
네트워크 인터페이스에 대 한 네트워크 인터페이스 IP 구성을 가져옵니다.

## 구문과

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzNetworkInterfaceIPConfig** Cmdlet은 Azure 네트워크 인터페이스에서 네트워크 인터페이스 IP 구성을 가져옵니다.

## 예제의

### 1: 네트워크 인터페이스의 IP 구성 가져오기
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

첫 번째 명령은 mynic 이라는 기존 네트워크 인터페이스를 가져와이를 변수 $nic 1에 저장 합니다. 두 번째 명령은이 네트워크 인터페이스의 ipconfig1 이라는 IP 구성을 가져옵니다.
    

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
이 cmdlet이 가져오는 네트워크 IP 구성의 이름을 지정 합니다.

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

### -NetworkInterface
이 cmdlet이 가져오는 네트워크 IP 구성을 포함 하는 **NetworkInterface** 개체를 지정 합니다.

```yaml
Type: PSNetworkInterface
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

### PSNetworkInterface
' NetworkInterface ' 매개 변수는 파이프라인에서 ' PSNetworkInterface ' 형식의 값을 허용 합니다.

## 출력

### PSNetworkInterfaceIPConfiguration에 대 한.

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹

## 관련 링크

[추가-AzNetworkInterfaceIpConfig](./Add-AzNetworkInterfaceIpConfig.md)

[새로운 AzNetworkInterfaceIpConfig](./New-AzNetworkInterfaceIpConfig.md)

[제거-AzNetworkInterfaceIpConfig](./Remove-AzNetworkInterfaceIpConfig.md)

[Set-AzNetworkInterfaceIpConfig](./Set-AzNetworkInterfaceIpConfig.md)


