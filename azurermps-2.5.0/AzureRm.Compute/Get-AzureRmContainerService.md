---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 5db21871b84801d57deebf98e27bbe153285631a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883173"
---
# Get-AzureRmContainerService

## SYNOPSIS
컨테이너 서비스를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Get-AzureRmContainerService** cmdlet은 컨테이너 서비스를 가져옵니다.
상태, 마스터 및 에이전트 수, 마스터 및 에이전트의 정규화 된 도메인 이름 등 컨테이너 서비스의 속성을 볼 수 있습니다.

## 예제의

### 예제 1: 컨테이너 서비스 가져오기
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

이 명령은 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.

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
이 cmdlet이 가져오는 컨테이너 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 가져오는 컨테이너 서비스의 리소스 그룹을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### PSContainerService의. m a.

## 상속자

## 관련 링크

[새로운 AzureRmContainerService](./New-AzureRmContainerService.md)

[제거-AzureRmContainerService](./Remove-AzureRmContainerService.md)

[업데이트-AzureRmContainerService](./Update-AzureRmContainerService.md)


