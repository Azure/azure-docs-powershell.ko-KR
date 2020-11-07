---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6a18c886ddddc30c82746ebe76d83d9477399755
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879014"
---
# Get-AzManagementGroupDeployment

## SYNOPSIS
관리 그룹에서 배포 가져오기

## 구문과

### GetByDeploymentName (기본값)
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzManagementGroupDeployment** cmdlet은 a 관리 그룹에서 배포를 가져옵니다.
*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.
기본적으로 **Get-AzManagementGroupDeployment** 는 관리 그룹의 모든 배포를 가져옵니다.

## 예제의

### 예제 1: 관리 그룹에서 모든 배포 가져오기
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

이 명령은 관리 그룹 "myMG"에 있는 모든 배포를 가져옵니다.

### 예제 2: 이름으로 배포 가져오기
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

이 명령은 관리 그룹 "myMG"에서 "Deploy01" 배포를 가져옵니다.
**새 AzManagementGroupDeployment** cmdlet을 사용 하 여 배포를 만들 때 이름을 지정할 수 있습니다.
이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.

### 예제 3: ID를 기준으로 배포 가져오기
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

이 명령은 관리 그룹 "myMG"에서 "Deploy01" 배포를 가져옵니다.

## 변수

### -ApiVersion
설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.
지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
배포의 정규화 된 리소스 Id입니다.
예:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupId
관리 그룹 id입니다.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
배포의 이름입니다.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## 상속자

## 관련 링크
