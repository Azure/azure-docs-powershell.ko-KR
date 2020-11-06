---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
ms.openlocfilehash: faaf8a0c614a1243a3e3812cd0b6e1202cc7e75b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532024"
---
# Export-AzureRmDataLakeStoreChildItemProperties

## SYNOPSIS
지정 된 경로에서 출력 경로로 전체 트리의 속성 (디스크 사용 및 Acl)을 내보냅니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### GetDiskUsage
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### GetAllProperties
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GetAclDump
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**Export-AzureRmDataLakeStoreChildItemProperties** 는 지정 된 디렉터리와 하위 디렉터리 및 파일에 대 한 ADLS space 사용량 또는/및 ACL 사용량을 보고 하는 데 사용 됩니다.

## 예제의

### 예제 1: 모든 하위 디렉터리 및 파일의 디스크 사용 및 ACL 사용량 가져오기
```
PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

/A 아래에 있는 모든 하위 디렉터리 및 파일의 디스크 사용 및 ACL 사용량을 가져옵니다. IncludeFile은 파일에 대 한 사용 현황도 보고 되도록 합니다.

### 예제 2: 일관성 있는 ACL이 숨겨진 모든 하위 디렉터리 및 파일에 대 한 ACL 사용 가져오기
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzureRmDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

/A 아래에 있는 모든 하위 디렉터리 및 파일의 ACL 사용을 가져옵니다. IncludeFile은 파일에 대 한 사용 현황도 보고 되도록 합니다. 이 경우 HideconsistentAcl 모든 자식의 acl이/a와 동일 하므로 해당 자식이 아니라/a의 Acl이 표시 됩니다. 이 플래그는 모든 acl이 루트와 동일한 경우 subtree의 acl 출력을 건너뜁니다.

## 변수

### -계정
파일 시스템 작업을 실행 하기 위한 Data Lake Store 계정

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
병렬로 처리 된 파일/디렉터리 수를 나타냅니다.
기본값은 시스템 사양에 따라 가장 좋은 노력으로 계산 됩니다.

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

### -GetAcl
루트 경로에서 시작 하는 acl을 검색 합니다.

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
루트 경로에서 시작 하는 디스크 사용량을 검색 합니다.

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
Acl이 전체 하위 트리 전체에서 동일한 경우 디렉터리 하위 트리를 표시 하지 않습니다. 이렇게 하면 Acl이 서로 다른 경로만 쉽게 볼 수 있습니다. 예를 들어/a/b의 모든 파일 및 폴더가 같은 경우 subtreeunder/a/b를 표시 하지 않고, IncludeFiles가 설정 되지 않은 경우에는 파일에 대 한 acl을 검색 하지 않고도 일관 된 Acl을 확인할 수 없기 때문에,이에 대 한 출력/a/b을 일관성 있는 ACL columnCannot으로 설정할 수 없습니다.

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
파일 수준에 통계 표시 (기본적으로 디렉터리 수준 정보만 표시 됨)

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
디스크 사용 또는 acl이 표시 될 때까지 루트 디렉터리의 최대 깊이

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
출력 파일의 경로입니다. 로컬 경로 또는 Adl 경로 일 수 있습니다. 기본적으로 로컬입니다. SaveToAdl가 pecified 이면 같은 계정의 ADL 경로입니다.

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
삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.

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
지정 된 Data Lake account에서 검색 해야 하는 경로입니다.
'/Folder/file.txt ' 형식으로 된 파일 또는 폴더 일 수 있으며, 여기에서 DNS 뒤의 첫 번째 '/'는 파일 시스템의 루트를 나타냅니다.

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
전달 된 후에는 덤프 파일을 ADL에 저장 합니다.
DumpFile 들으며는이 경우 ADL 경로로 사용할 수 있습니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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

### System. 문자열

### DataLakeStore. DataLakeStorePathInstance/.

### System.webserver 매개 변수

### 시스템. i i.

## 출력

### 시스템 부울

## 상속자

## 관련 링크
