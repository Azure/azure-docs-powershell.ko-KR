---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490572"
---
# Get-AzDeploymentOperation

## SYNOPSIS
배포 작업 얻기

## 구문

### GetByDeploymentName(기본값)
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzDeploymentOperation** cmdlet은 특정 배포에 실패한 정확한 작업에 대한 자세한 정보를 식별하고 제공하기 위해 배포의 일부인 모든 작업을 나열합니다.
또한 각 배포 작업에 대한 응답 및 요청 콘텐츠를 보여 주어도 됩니다.
이는 포털의 배포 세부 정보에 제공된 동일한 정보입니다.

요청 및 응답 콘텐츠를 얻습니다. **New-AzDeployment를** 통해 배포를 제출할 때 설정을 사용하도록 설정하세요.
잠재적으로 배포 작업을 검색할 때 반환되는 리소스 속성 또는 **listKeys** 작업에 사용되는 암호와 같은 비밀을 기록하고 노출할 수 있습니다.
이 설정 및 사용하도록 설정하는 방법에 대한 자세한 내용은 템플릿 배포에 대한 New-AzDeployment 및 디버깅을 ARM 참조

## 예제

### 예제 1: 배포 이름을 지정한 배포 작업 얻기
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

현재 구독 범위에서 이름이 "test"인 배포 작업을 얻습니다.

### 예제 2: 배포를 시작하고 배포 작업을 얻습니다.
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

이 명령은 현재 구독 범위에서 배포 "테스트"를 수행하고 해당 배포 작업을 얻습니다.

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

### -DeploymentName
배포 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentObject
배포 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperationId
배포 작업 ID입니다.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
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

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD

## 출력

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation

## 참고 사항

## 관련 링크
