---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 4a2293384cdf2cf579458d05c112469d096bfd9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354225"
---
# Set-AzSynapseSqlActiveDirectoryAdministrator

## SYNOPSIS
Synapse Analytics 풀에 대한 Azure AD SQL 프로비전합니다.

## 구문

### SetByNameParameterSet(기본값)
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByInputObjectParameterSet
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByResourceIdParameterSet
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet은 현재 구독에서 Azure Synapse Analytics 작업 영역의 Azure AD(Azure Active Directory) 관리자를 프로비전합니다.
한 번의 관리자만 프로비전할 수 있습니다.
다음 Azure AD 멤버를 Synapse Analytics 작업 영역 관리자로 프로비전할 수 있습니다.
- Azure AD의 네이티브 멤버 
- Azure AD의 페더리된 멤버 
- 네이티브 또는 페더리된 멤버인 다른 Azure AD에서 가져온 멤버 
- 보안 그룹으로 만든 Azure AD 그룹(예: Outlook.com, Hotmail.com 또는 Live.com 도메인의 그룹)은 관리자로 지원되지 않습니다.
다른 게스트 계정(예: Gmail.com 또는 Yahoo.com 도메인)은 관리자로 지원되지 않습니다.
관리자 권한으로 전용 Azure AD 그룹을 프로비전하는 것이 좋습니다.

## 예제

### 예제 1
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

이 명령은 ContosoWorkspace라는 작업 영역의 DBAS라는 Azure AD 관리자 그룹을 프로비전합니다.

### 예제 2
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

이 명령은 ContosoWorkspace라는 작업 영역의 DBAS라는 Azure AD 관리자 그룹을 프로비전합니다.
이렇게 하면 그룹의 표시 이름이 고유하지 않은 경우에도 명령이 성공합니다.

## PARAMETERS

### -AsJob
백그라운드에서 cmdlet 실행

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

### -DisplayName
권한을 부여할 사용자 또는 그룹의 표시 이름을 지정합니다.
이 표시 이름은 현재 구독과 연결된 Active Directory에 있어야 합니다.

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

### -InputObject
일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
권한을 부여할 Azure Active Directory에서 사용자 또는 그룹의 개체 ID를 지정합니다.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Synapse 작업 영역의 리소스 식별자입니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Synapse 작업 영역의 이름입니다.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

## 출력

### Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo

## 참고 사항

## 관련 링크
