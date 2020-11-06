---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: d7e3055c6443faa2c85d63e6cfdb611cb7d2eb41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523812"
---
# New-AzureRmDeploymentManagerServiceTopology

## SYNOPSIS
새 서비스 토폴로지를 만듭니다.

## 구문과

```
New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**새 AzureRmDeploymentManagerServiceTopology** cmdlet은 서비스 토폴로지를 만듭니다.

반환 된 ServiceTopology 개체를 로컬로 수정한 다음 Set-AzureRmDeploymentManagerServiceTopology cmdlet을 사용 하 여 토폴로지에 변경 내용을 적용할 수 있습니다.
반환 된 개체 

반환 된 개체에는 롤아웃 리소스에서 참조할 수 있는 ResourceId 필드가 있으며,이는이 서비스 토폴로지에 선언 된 서비스가 롤아웃에 배포 됨을 나타냅니다.

## 예제의

### 예제 1
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

이 cmdlet은 이름 ContosoServiceTopology 및 in 위치 중앙 US를 사용 하 여 리소스 그룹 ContosoResourceGroup에 새 서비스 토폴로지를 만듭니다. 아티팩트 원본 ResourceId는이 토폴로지의 서비스 단위 정의에 필요한 아티팩트를 지정 된 아티팩트 원본에서 읽어야 함을 나타냅니다.

### 예제 2
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

이 cmdlet은 이름 ContosoServiceTopology 및 in 위치 중앙 US를 사용 하 여 리소스 그룹 ContosoResourceGroup에 새 서비스 토폴로지를 만듭니다. 아티팩트 원본 참조가 없으면이 토폴로지의 서비스 단위 정의에 필요한 아티팩트가 서비스 단위에서 절대 SAS Uri로 제공 됨을 나타냅니다.

## 변수

### -ArtifactSourceId
토폴로지를 구성 하는 아티팩트가 저장 되는 아티팩트 소스의 식별자입니다.

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

### -위치
토폴로지의 위치입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
토폴로지 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
리소스 태그를 나타내는 해시 테이블입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### PSServiceTopologyResource-. m i 매니저.

## 상속자

## 관련 링크

[Get-AzureRmDeploymentManagerServiceTopology](./Get-AzureRmDeploymentManagerServiceTopology.md)

[제거-AzureRmDeploymentManagerServiceTopology](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[Set-AzureRmDeploymentManagerServiceTopology](./Set-AzureRmDeploymentManagerServiceTopology.md)