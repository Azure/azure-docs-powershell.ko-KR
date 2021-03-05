---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 0f43c372901dbfd571343584f0ca8479d5b7081e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013664"
---
# Export-AzDataLakeStoreChildItemProperty

## SYNOPSIS
지정된 경로에서 출력 경로로 전체 트리에 대한 속성(디스크 사용량 및 Acl)을 내보낼 수 있습니다.

## 구문

### GetDiskUsage
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### GetAllProperties
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GetAclDump
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Export-AzDataLakeStoreChildItemProperty는** 주어진 디렉터리에 대한 ADLS 공간 사용량 또는/및 ACL 사용량을 보고하는 데 사용하며 하위 디렉터리 및 파일입니다.

## 예제

### 예제 1: 모든 하위 디렉터리 및 파일에 대한 디스크 사용량 및 ACL 사용량을 얻습니다.
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

/a 아래에서 모든 하위 디렉터리 및 파일에 대한 디스크 사용량 및 ACL 사용량을 얻습니다. IncludeFile을 사용하면 파일에 대한 사용량이 보고됩니다.

### 예제 2: 일관된 ACL이 숨겨져 있는 모든 하위 및 파일에 대한 ACL 사용량을 얻습니다.
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

/a 아래에서 모든 하위 및 파일에 대한 ACL 사용량을 얻습니다. IncludeFile은 파일에 대한 사용량도 보고되도록 합니다. 이 경우 HideconsistentAcl은 모든 자식이 /a와 동일한 acl을 포함하기 때문에 자식이 아닌 /a의 Acl을 보여 주게됩니다. 이 플래그는 모든 acls가 루트와 같을 경우 하위트리의 acl 출력을 생략합니다.

## 매개 변수

### -Account
Data Lake Store 계정에서 파일계산 작업을 실행합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -동시성
병렬로 처리된 파일/감독의 수를 나타냅니다.
기본값은 시스템 사양에 따라 최상의 노력으로 계산됩니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -GetAcl
루트 경로에서 시작하여 acl을 검색합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GetDiskUsage
루트 경로에서 시작하여 디스크 사용량을 검색합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HideConsistentAcl
전체 하위트리에서 ACL이 동일한 경우 디렉터리 하위트리를 표시하지 않습니다. 이렇게 하면 ACL이 다른 경로만 쉽게 볼 수 있습니다. 예를 들어 /a/b 아래 모든 파일 및 폴더가 동일할 경우 하위treeunder /a/b를 표시하지 않고 일관된 ACL 열에 'True'가 포함된 출력 /a/b만 설정되지 않습니다. IncludeFiles가 설정되지 않은 경우 파일에 대한 acl을 검색하지 않고 일관된 Acl을 찾을 수 없습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFile
파일 수준에서 통계 표시(기본적으로 디렉터리 수준 정보만 표시)

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaximumDepth
디스크 사용량 또는 acl이 표시될 때까지 루트 디렉터리의 최대 깊이

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputPath
출력 파일에 대한 경로입니다. 로컬 경로 또는 Adl 경로일 수 있습니다. 기본적으로 로컬입니다. SaveToAdl을 지정한 경우 동일한 계정의 ADL 경로입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
삭제 작업의 결과를 나타내는 부울 응답을 반환해야 한다고 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
검색해야 하는 지정된 Data Lake 계정의 경로입니다.
파일 또는 폴더 형식 '/folder/file.txt'일 수 있습니다. 여기서 DNS 다음의 첫 번째 '/'는 파일 시스템의 루트를 나타냅니다.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SaveToAdl
통과하면 덤프 파일을 ADL에 저장합니다.
이 경우 DumpFile wil은 ADL 경로가 됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance

### System.Management.Automation.SwitchParameter

### System.Int32

## 출력

### System.Boolean

## 참고 사항

## 관련 링크
