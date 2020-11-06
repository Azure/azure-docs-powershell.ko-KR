---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: 5a9a6eba53a455da2efb7ee98d990d6b39538518
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534688"
---
# Set-AzureRmResourceGroup

## SYNOPSIS
리소스 그룹을 수정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### SetByResourceGroupName (기본값)
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Set-AzureRmResourceGroup** cmdlet은 리소스 그룹의 속성을 수정 합니다.
이 cmdlet을 사용 하 여 리소스 그룹에 적용 된 Azure 태그를 추가, 변경 또는 삭제할 수 있습니다.
*Name* 매개 변수를 지정 하 여 리소스 그룹을 식별 하 고 *Tag* 매개 변수를 지정 하 여 태그를 수정 합니다.

이 cmdlet을 사용 하 여 리소스 그룹의 이름을 변경할 수 없습니다.

## 예제의

### 예제 1: 리소스 그룹에 태그 적용
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

이 명령은 해당 값이 포함 된 부서 태그를 기존 태그가 없는 리소스 그룹에 적용 합니다.

### 예제 2: 리소스 그룹에 태그 추가
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

이 예제에서는 승인 값이 있는 상태 태그와 기존 태그가 있는 리소스 그룹에 FY2016 태그를 추가 합니다. 지정 하는 태그가 기존 태그를 대체 하기 때문에 새 태그 컬렉션에 기존 태그를 포함 해야 하며, 그렇지 않은 경우에는 없어집니다.

첫 번째 명령은 ContosoRG 리소스 그룹을 가져온 다음 도트 메서드를 사용 하 여 해당 태그 속성의 값을 가져옵니다. 명령이 $Tags 변수에 태그를 저장 합니다.

두 번째 명령은 $Tags 변수의 태그를 가져옵니다.

세 번째 명령은 + = 대입 연산자를 사용 하 여 $Tags 변수의 태그 배열에 Status 및 FY2016 태그를 추가 합니다.

네 번째 명령은 **Set-AzureRmResourceGroup** 의 *Tag* 매개 변수를 사용 하 여 $Tags 변수의 태그를 ContosoRG 리소스 그룹에 적용 합니다.

다섯 번째 명령은 ContosoRG 리소스 그룹에 적용 된 모든 태그를 가져옵니다. 출력에는 리소스 그룹에 부서 태그와 두 개의 새 태그, 상태 및 FY2015이 표시 됩니다.

### 예제 3: 리소스 그룹에 대 한 모든 태그 삭제
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

이 명령은 ContosoRG 리소스 그룹에서 모든 태그를 삭제 하는 빈 해시 테이블 값을 사용 하 여 *Tag* 매개 변수를 지정 합니다.

## 변수

### -ApiVersion
리소스 공급자가 지 원하는 API 버전을 지정 합니다.
기본 버전 외의 다른 버전을 지정할 수 있습니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -Id
수정할 리소스 그룹의 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
수정할 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예를 들어:

@ {key0 = "value0", key1 = $null, key2 = "value2"}

태그는 사용자가 만들고 리소스 및 리소스 그룹에 적용할 수 있는 이름-값 쌍입니다. 리소스 및 그룹에 태그를 할당 한 후에 Get-AzureRmResourceGroup Get-AzureRmResource의 *tag* 매개 변수를 사용 하 여 태그 이름 또는 이름 및 값을 기준으로 리소스와 그룹을 검색할 수 있습니다. 태그를 사용 하 여 부서나 비용 센터 등의 리소스를 분류 하거나 자원에 대 한 메모 또는 설명을 추적할 수 있습니다.

태그를 추가 하거나 변경 하려면 리소스 그룹에 대 한 태그 컬렉션을 바꿔야 합니다. 태그를 삭제 하려면 삭제 하려는 태그를 제외 하 고 **AzureRmResourceGroup** 에서 리소스 그룹에 현재 적용 된 모든 태그가 있는 해시 테이블을 입력 합니다. 리소스 그룹에서 모든 태그를 삭제 하려면 빈 해시 테이블 ()을 지정 `@{}` 합니다.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### Microsoft. .Resources. PSResourceGroup.

## 상속자

## 관련 링크

[Get-AzureRmResource](./Get-AzureRmResource.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[새로운 AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[제거-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)
