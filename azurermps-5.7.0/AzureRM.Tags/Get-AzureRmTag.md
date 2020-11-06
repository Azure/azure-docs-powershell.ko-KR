---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 79fa1522ed0eec95a1e388ed5d113cf98ad7f525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533544"
---
# Get-AzureRmTag

## SYNOPSIS
미리 정의 된 Azure 태그를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmTag** cmdlet은 구독에서 미리 정의 된 Azure 태그를 가져옵니다.
이 cmdlet은 태그에 대 한 기본 정보를 반환 합니다.
모든 출력 개체에는 태그와 값이 적용 된 리소스 및 리소스 그룹 수를 나타내는 Count 속성이 포함 됩니다.

**AzureRMTag** 의 일부인 azure tags 모듈은 미리 정의 된 Azure 태그를 관리 하는 데 도움이 될 수 있습니다.
Azure 태그는 사용자가 Azure 리소스 및 리소스 그룹 (예: 부서나 비용 센터)을 분류 하거나 리소스 및 그룹에 대 한 메모 또는 설명을 추적 하는 데 사용할 수 있는 이름-값 쌍입니다.

한 단계에서 태그를 정의 하 고 적용할 수 있지만, 미리 정의 된 태그를 사용 하면 구독의 태그에 대 한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.
구독에 미리 정의 된 태그가 포함 되어 있는 경우에는 구독에 있는 리소스나 리소스 그룹에 정의 되지 않은 태그나 값을 적용할 수 없습니다.

미리 정의 된 태그를 만들려면 New-AzureRmTag cmdlet을 사용 합니다.
리소스 그룹에 미리 정의 된 태그를 적용 하려면 New-AzureRmTag cmdlet의 *tag* 매개 변수를 사용 합니다.
특정 태그 이름 또는 이름과 값에 대 한 리소스 그룹을 검색 하려면 Get-AzureRMResourceGroup cmdlet의 *tag* 매개 변수를 사용 합니다.

## 예제의

### 예제 1: 미리 정의 된 모든 태그 가져오기
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

이 명령은 구독에서 미리 정의 된 모든 태그를 가져옵니다.
Count 속성에는 구독의 리소스 및 리소스 그룹에 태그가 적용 된 횟수가 표시 됩니다.

### 예제 2: 이름으로 태그 가져오기
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

이 명령은 부서 태그 및 해당 값에 대 한 자세한 정보를 가져옵니다.
Count 속성은 태그 및 각 값이 구독의 리소스 및 리소스 그룹에 적용 된 횟수를 보여 줍니다.

### 예제 3: 모든 태그 값 가져오기
```
PS C:\>Get-AzureRmTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

이 명령은 *자세한* 매개 변수를 사용 하 여 구독에 미리 정의 된 모든 태그에 대 한 자세한 정보를 가져옵니다.
*자세한* 매개 변수를 사용 하는 것은 모든 태그에 *Name* 매개 변수를 사용 하는 것과 같습니다.

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

### -세부 정보
이 작업이 태그 값에 대 한 정보를 출력에 추가 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
가져올 태그의 이름을 지정 합니다.
기본적으로 **AzureRmTag** 에서는 구독에 있는 모든 미리 정의 된 태그에 대 한 기본 정보를 가져옵니다.
*Name* 매개 변수를 지정 하면 *Detailed* 매개 변수는 아무런 영향을 주지 않습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### PSTag, Microsoft Azure. Commands.. m a m

## 상속자

## 관련 링크

[새로운 AzureRmTag](./New-AzureRmTag.md)

[제거-AzureRmTag](./Remove-AzureRmTag.md)


