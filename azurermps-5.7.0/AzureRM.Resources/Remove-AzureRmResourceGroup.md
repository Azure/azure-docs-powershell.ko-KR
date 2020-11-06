---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: ce028e52d893372f4a668a278466d4cdc51655f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531661"
---
# Remove-AzureRmResourceGroup

## SYNOPSIS
리소스 그룹을 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### RemoveByResourceGroupName (기본값)
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceGroupId
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹과 해당 리소스를 제거 합니다.
리소스를 삭제 하 되 리소스 그룹을 유지 하려면 Remove-AzureRmResource cmdlet을 사용 합니다.

## 예제의

### 예제 1: 리소스 그룹 제거
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

이 명령은 구독에서 ContosoRG01 리소스 그룹을 제거 합니다.
Cmdlet에서 확인을 요청 하 고 출력을 반환 하지 않습니다.

### 예제 2: 확인 하지 않고 리소스 그룹 제거
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

이 명령은 Get-AzureRmResourceGroup cmdlet을 사용 하 여 리소스 그룹 ContosoRG01을 얻은 다음 pipeline 연산자를 사용 하 여 **Remove-AzureRmResourceGroup** 에 전달 합니다.
*Verbose* 공용 매개 변수는 연산에 대 한 상태 정보를 가져오며 *Force* 매개 변수는 확인 메시지를 표시 하지 않습니다.

### 예제 3: 모든 리소스 그룹 제거
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

이 명령은 **AzureRmResourceGroup** cmdlet을 사용 하 여 모든 리소스 그룹을 가져와 해당 파이프라인 연산자를 사용 하 여 **Remove-AzureRmResourceGroup** 에 전달 합니다.

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

### -AsJob
백그라운드에서 cmdlet 실행

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

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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

### -Id
제거할 리소스 그룹의 ID를 지정 합니다.
와일드 카드 문자는 허용 되지 않습니다.

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
제거할 리소스 그룹의 이름을 지정 합니다.
와일드 카드 문자는 허용 되지 않습니다.

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### 않아야

## 상속자

## 관련 링크

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[새로운 AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)


