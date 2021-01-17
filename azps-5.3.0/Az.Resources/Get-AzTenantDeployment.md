---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490463"
---
# Get-AzTenantDeployment

## SYNOPSIS
테넌트 범위에서 배포를 구합니다.

## 구문

### GetByDeploymentName(기본값)
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzTenantDeployment** cmdlet은 테넌트 범위에서 배포를 얻습니다.
결과를 필터링할 *이름* 또는 *ID* 매개 변수를 지정합니다.
기본적으로 **Get-AzTenantDeployment는** 테넌트 범위에서 모든 배포를 얻습니다.

## 예제

### 예제 1: 테넌트 범위에서 모든 배포를 얻습니다.
```
PS C:\>Get-AzTenantDeployment
```

이 명령은 현재 테넌트 범위에서 모든 배포를 얻습니다.

### 예제 2: 이름으로 배포하기
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

이 명령은 현재 테넌트 범위에서 "Deploy01" 배포를 얻습니다.
**New-AzTenantDeployment** cmdlet을 사용하여 배포를 만들 때 이름을 할당할 수 있습니다.
이름을 할당하지 않는 경우 cmdlet은 배포를 만드는 데 사용되는 템플릿에 따라 기본 이름을 제공합니다.

### 예제 3: ID로 배포하기
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

이 명령은 테넌트 범위에서 "Deploy01" 배포를 얻습니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
배포의 정식 리소스 ID입니다.
예: /providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
배포의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD

## 참고 사항

## 관련 링크
