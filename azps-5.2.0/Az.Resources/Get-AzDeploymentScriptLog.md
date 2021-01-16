---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325345"
---
# Get-AzDeploymentScriptLog

## SYNOPSIS
배포 스크립트 실행의 로그를 얻습니다.

## 구문

### GetDeploymentScriptLogByName(기본값)
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetDeploymentScriptLogByResourceId
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetDeploymentScriptLogByInputObject
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzDeploymentScriptLog** cmdlet은 배포 스크립트 실행의 로그를 얻습니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

리소스 그룹 DS-TestRG에서 MyDeploymentScript 이름이 있는 배포 스크립트의 로그를 얻습니다.

### 예제 2
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

리소스 그룹 DS-TestRG에서 MyDeploymentScript 이름이 있는 배포 스크립트 로그의 마지막 3줄을 얻습니다.

### 예제 3
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

첫 번째 명령은 리소스 그룹 DS-TestRG에서 MyDeploymentScript 이름이 있는 배포 스크립트를 얻습니다.
두 번째 명령은 주어진 배포 스크립트의 로그를 얻습니다.

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

### -DeploymentScriptObject
배포 스크립트 PowerShell 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeploymentScriptResourceId
배포 스크립트의 정식 리소스 ID입니다.
예: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
배포 스크립트의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tail
출력을 마지막 n줄로 제한

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript

## 출력

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog

## 참고 사항

## 관련 링크
