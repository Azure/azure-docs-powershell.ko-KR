---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: cd9700a633f1a9c09c5fafd060d318b35eaeaabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536476"
---
# New-AzureRmTag

## SYNOPSIS
미리 정의 된 Azure 태그를 만들거나 기존 태그에 값을 추가 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmTag** cmdlet은 미리 정의 된 선택적 값을 사용 하 여 미리 정의 되어 있는 Azure 태그를 만듭니다.
또한 기존에 미리 정의 된 태그에 다른 값을 추가 하는 데 사용할 수 있습니다.
미리 정의 된 태그를 만들려면 고유한 태그 이름을 입력 합니다.
미리 정의 된 기존 태그에 값을 추가 하려면 기존 태그의 이름과 새 값을 지정 합니다.
이 cmdlet은 새 태그 또는 수정 된 태그가 해당 값과 적용 된 리소스 수를 나타내는 개체를 반환 합니다.
**새로운 AzureRmTag** 의 일부인 azure tags 모듈은 미리 정의 된 Azure 태그를 관리 하는 데 도움이 될 수 있습니다.
Azure 태그는 사용자가 Azure 리소스 및 리소스 그룹 (예: 부서나 비용 센터)을 분류 하거나 리소스 및 그룹에 대 한 메모 또는 설명을 추적 하는 데 사용할 수 있는 이름-값 쌍입니다.
한 단계에서 태그를 정의 하 고 적용할 수 있지만, 미리 정의 된 태그를 사용 하면 구독의 태그에 대 한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.
리소스 또는 리소스 그룹에 미리 정의 된 태그를 적용 하려면 New-AzureRmTag cmdlet의 *tag* 매개 변수를 사용 합니다.
지정 된 태그 이름이 나 이름 및 값을 사용 하 여 리소스 그룹을 검색 하려면 Get-AzureRMResourceGroup cmdlet의 *tag* 매개 변수를 사용 합니다.
모든 태그에는 이름이 있습니다.
값은 선택 사항입니다.
미리 정의 된 Azure 태그에는 여러 값이 포함 될 수 있지만 리소스 또는 리소스 그룹에 태그를 적용 하는 경우 태그 이름과 해당 값 중 하나만 적용 됩니다.
예를 들어 재무, 인적 자원 등의 각 부서에 대 한 값을 사용 하 여 미리 정의 된 부서 태그를 만들 수 있습니다.
자원에 부서 태그를 적용 하는 경우 재무와 같은 미리 정의 된 값을 하나만 적용 합니다.

## 예제의

### 예제 1: 미리 정의 된 태그 만들기
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   FY2015
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

이 명령은 FY2015 이라는 미리 정의 된 태그를 만듭니다.
이 태그에는 값이 없습니다.
값이 없는 태그를 리소스나 리소스 그룹에 적용 하거나, **New-AzureRmTag** 를 사용 하 여 태그에 값을 추가할 수 있습니다.
리소스 또는 리소스 그룹에 태그를 적용 하는 경우 값을 지정할 수도 있습니다.

### 예제 2: 값을 사용 하 여 미리 정의 된 태그 만들기
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

이 명령은 재무 값이 포함 된 부서별 이라는 미리 정의 된 태그를 만듭니다.

### 예제 3: 미리 정의 된 태그에 값 추가
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

이러한 명령을 사용 하면 두 값이 있는 부서별 이라는 미리 정의 된 태그를 만듭니다.
태그 이름이 있으면 새 항목을 만드는 대신 **AzureRmTag** 에서 기존 태그에 값을 추가 합니다.

### 예제 4: 미리 정의 된 태그 사용
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

이 예제의 명령은 미리 정의 된 태그를 만들고 사용 합니다.

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

### -이름
태그 이름을 지정 합니다.
미리 정의 된 새 태그를 만들려면 고유한 이름을 입력 합니다.
기존 태그에 값을 추가 하려면 기존 태그의 이름을 입력 합니다.
미리 정의 된 기존 태그에 지정 된 이름이 있는 경우 새 태그를 만드는 대신 해당 이름의 태그에 지정 된 값이 있는 경우 **AzureRmTag** 를 추가 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -값
태그 값을 지정 합니다.
미리 정의 된 태그에 여러 값이 있을 수 있지만 각 명령에 하나의 값만 입력할 수 있습니다.
태그에 값이 없는 이름이 있을 수 있으므로이 매개 변수는 선택 사항입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### PSTag를 통해 서의 일반.

## 상속자

## 관련 링크

[Get-AzureRmTag](./Get-AzureRmTag.md)

[제거-AzureRmTag](./Remove-AzureRmTag.md)


