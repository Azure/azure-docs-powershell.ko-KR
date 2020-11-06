---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: ccb0b4afdf39510461dd0f6627748492ba22818f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530706"
---
# New-AzureRmResourceGroup

## SYNOPSIS
Azure 리소스 그룹을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmResourceGroup** Cmdlet은 Azure 리소스 그룹을 만듭니다.

이름과 위치만 사용 하 여 리소스 그룹을 만든 다음 New-AzureRmResource cmdlet을 사용 하 여 리소스 그룹에 추가할 리소스를 만들 수 있습니다.

기존 리소스 그룹에 배포를 추가 하려면 New-AzureRmResourceGroupDeployment cmdlet을 사용 합니다. 기존 리소스 그룹에 리소스를 추가 하려면 **새 AzureRmResource** cmdlet을 사용 합니다. Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스 또는 웹 사이트)입니다. Azure 리소스 그룹은 하나의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.

## 예제의

### 예제 1: 빈 리소스 그룹 만들기
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US"
```

이 명령은 리소스가 없는 리소스 그룹을 만듭니다. **새로운 AzureRmResource** 또는 **AzureRmResourceGroupDeployment** cmdlet을 사용 하 여 리소스 및 배포를이 리소스 그룹에 추가할 수 있습니다.

### 예제 2: 태그를 사용 하 여 리소스 그룹 만들기
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US" -Tag @{"Empty"=$null; "Department"="Marketing"}
```

이 명령은 빈 리소스 그룹을 만듭니다. 이 명령은 예제 1의 명령과 같으며 리소스 그룹에 태그를 할당 한다는 점이 다릅니다. 비어 있는 첫 번째 태그는 리소스가 없는 리소스 그룹을 식별 하는 데 사용할 수 있습니다. 두 번째 태그는 부서 라는 이름이 며 마케팅 값이 있습니다. 이 예제와 같은 태그를 사용 하 여 관리 또는 예산 책정에 대 한 리소스 그룹을 분류할 수 있습니다.

## 변수

### -ApiVersion
리소스 공급자가 지 원하는 API 버전을 지정 합니다.
기본 버전 외의 다른 버전을 지정할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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

### -위치
리소스 그룹의 위치를 지정 합니다. Azure 데이터 센터 위치 (예: 서쪽 미국 또는 동남 아시아)를 지정 합니다. 임의의 위치에 리소스 그룹을 배치할 수 있습니다. 리소스 그룹은 Azure 구독에 같은 위치에 있거나 리소스와 같은 위치에 있을 필요가 없습니다.

각 리소스 형식을 지 원하는 위치를 확인 하려면 *Providernamespace* 매개 변수와 함께 Get-AzureRmResourceProvider cmdlet을 사용 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
리소스 그룹의 이름을 지정 합니다. 리소스 이름은 구독에서 고유 해야 합니다. 해당 이름을 가진 리소스 그룹이 이미 있는 경우 기존 리소스 그룹을 바꾸기 전에 명령에서 확인을 요청 하는 메시지가 표시 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.

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

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예를 들어:

@ {key0 = "value0", key1 = $null, key2 = "value2"}

태그를 추가 하거나 변경 하려면 리소스 그룹에 대 한 태그 컬렉션을 바꿔야 합니다.

리소스 및 그룹에 태그를 할당 한 후에 Get-AzureRmResourceGroup Get-AzureRmResource의 *tag* 매개 변수를 사용 하 여 태그 이름 또는 이름 및 값을 기준으로 리소스와 그룹을 검색할 수 있습니다. 태그를 사용 하 여 부서나 비용 센터 등의 리소스를 분류 하거나 자원에 대 한 메모 또는 설명을 추적할 수 있습니다.

미리 정의 된 태그를 가져오려면 Get-AzureRMTag cmdlet을 사용 합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
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

### 않아야

## 출력

### ResourceManagement. PSResourceGroup.

## 상속자

## 관련 링크

[Get-AzureRmResourceProvider](./Get-AzureRmResourceProvider.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[새로운 AzureRmResource](./New-AzureRmResource.md)

[새로운 AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[제거-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)
