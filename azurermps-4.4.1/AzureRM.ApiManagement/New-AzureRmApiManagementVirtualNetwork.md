---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525792"
---
# New-AzureRmApiManagementVirtualNetwork

## SYNOPSIS
PsApiManagementVirtualNetwork의 인스턴스를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmApiManagementVirtualNetwork** Cmdlet은 **PsApiManagementVirtualNetwork** 의 인스턴스를 만드는 도우미 명령입니다.
이 명령은 **Set-AzureRMApiManagementVirtualNetworks** cmdlet과 함께 사용 됩니다.

## 예제의

### 예제 1: 가상 네트워크 만들기
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

이 예제에서는 가상 네트워크를 만든 다음 **AzureRmApiManagementVirtualNetworks** cmdlet을 호출 합니다.

## 변수

### -위치
이 cmdlet이 인스턴스를 만드는 가상 네트워크의 위치를 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 대한민국 미국 중부
- 미국 중부 US
- 중부 US
- 유럽 서유럽
- 동유럽
- 미국 서 부
- 미국 동부
- 미국 동부 2
- 일본 동부
- 일본 서쪽
- 브라질 남부
- 동남 아시아
- 동아시아
- 오스트레일리아 동부
- 오스트레일리아 남동쪽

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

### -SubnetResourceId
가상 네트워크의 서브넷 리소스 ID를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### ApiManagement. PsApiManagementVirtualNetwork/.

## 상속자

## 관련 링크

