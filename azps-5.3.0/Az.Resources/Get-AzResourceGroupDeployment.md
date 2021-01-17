---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490500"
---
# Get-AzResourceGroupDeployment

## SYNOPSIS
리소스 그룹의 배포를 얻습니다.

## 구문

### GetByResourceGroupDeploymentName(기본값)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzResourceGroupDeployment** cmdlet은 Azure 리소스 그룹의 배포를 얻습니다.
결과를 필터링할 *이름* 또는 *ID* 매개 변수를 지정합니다.
기본적으로 **Get-AzResourceGroupDeployment는** 지정된 리소스 그룹에 대한 모든 배포를 얻습니다.
Azure 리소스는 데이터베이스 서버, 데이터베이스 또는 웹 사이트와 같은 사용자 관리 Azure 엔터티입니다.
Azure 리소스 그룹은 단위로 배포되는 Azure 리소스의 컬렉션입니다.
배포는 리소스 그룹의 리소스를 사용할 수 있도록 하는 작업입니다.
Azure 리소스 및 Azure 리소스 그룹에 대한 자세한 내용은 New-AzResourceGroup 참조하세요.
추적에 이 cmdlet을 사용할 수 있습니다.
디버깅의 경우 이 cmdlet을 Get-AzLog cmdlet을 사용 합니다.

## 예제

### 예제 1: 리소스 그룹에 대한 모든 배포를 얻습니다.
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

이 명령은 ContosoLabsRG 리소스 그룹에 대한 모든 배포를 얻습니다.
출력은 갤러리 템플릿을 사용한 WordPress 블로그에 대한 배포를 보여줍니다.

### 예제 2: 이름으로 배포하기
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

이 명령은 ContosoLabsRG 리소스 그룹의 DeployWebsite01 배포를 얻습니다.
**New-AzResourceGroup** 또는 **New-AzResourceGroupDeployment** cmdlet을 사용하여 배포에 이름을 할당할 수 있습니다.
이름을 할당하지 않는 경우 cmdlet은 배포를 만드는 데 사용되는 템플릿에 따라 기본 이름을 제공합니다.

### 예제 3: 모든 리소스 그룹의 배포를 얻습니다.
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

이 명령은 Get-AzResourceGroup cmdlet을 사용하여 구독의 모든 리소스 그룹을 얻습니다.
이 명령은 파이프라인 연산자를 사용하여 리소스 그룹을 현재 cmdlet에 전달합니다.
현재 cmdlet은 구독의 모든 리소스 그룹의 모든 배포를하고 결과를 Format-Table cmdlet에 전달하여 **ResourceGroupName,** **DeploymentName** 및 **ProvisioningState** 속성 값을 표시합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
얻을 리소스 그룹 배포의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
얻을 배포의 이름을 지정합니다.
와일드카드 문자는 허용되지 않습니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.

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

### -ResourceGroupName
리소스 그룹의 이름을 지정합니다.
cmdlet은 이 매개 변수가 지정하는 리소스 그룹에 대한 배포를 얻습니다.
와일드카드 문자는 허용되지 않습니다.
이 매개 변수는 필수로, 각 명령에서 하나의 리소스 그룹만 지정할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment

## 참고 사항

## 관련 링크

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


