---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
ms.openlocfilehash: d51528cab51e4e6fe6cda428e25965d65c449c4b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882378"
---
# Get-AzureRmVMRunCommandDocument

## SYNOPSIS
실행 명령 문서를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
실행 명령 문서를 가져옵니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

' Westus '의 ' RunPowerShellScript '에 대 한 특정 실행 명령 문서를 가져옵니다.


Get-AzureRmVMRunCommandDocument 위치 $loc

### 예제 2
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

' Westus '에 사용 가능한 모든 실행 명령을 나열 합니다.

## 변수

### -CommandId
명령 id입니다.

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

### -위치
실행 명령이 쿼리 되는 위치입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. a. m a. 모델. a PSRunCommandDocument

## 상속자

## 관련 링크

