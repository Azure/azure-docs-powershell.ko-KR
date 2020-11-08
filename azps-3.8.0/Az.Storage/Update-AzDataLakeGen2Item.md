---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034961"
---
# Update-AzDataLakeGen2Item

## SYNOPSIS
속성, 메타 데이터, 사용 권한, ACL 및 owner에 대 한 파일 또는 디렉터리를 업데이트 합니다.

## 구문과

### ReceiveManual (기본값)
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ItemPipeline
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzDataLakeGen2Item** cmdlet은 속성, 메타 데이터, 사용 권한, ACL 및 owner에 대 한 파일 또는 디렉터리를 업데이트 합니다.
이 cmdlet은 저장소 계정에 대해 계층적 네임 스페이스를 사용 하는 경우에만 작동 합니다. "-EnableHierarchicalNamespace $true"를 사용 하 여 "New-AzStorageAccount" cmdlet을 실행 하 여 이러한 종류의 계정을 만들 수 있습니다.

## 예제의

### 예제 1: ACL 항목이 3 개 있는 ACL 개체를 만들고 파일 시스템의 모든 항목에 대 한 ACL을 재귀적으로 업데이트 합니다.
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

이 명령은 먼저 3 개의 acl 항목이 있는 ACL 개체를 만들고 (-InputObject 매개 변수를 사용 하 여 기존 acl 개체에 acl 항목을 추가 하려면) filesystem의 모든 항목을 가져오고 항목의 ACL을 업데이트 합니다.

### 예제 2: 파일의 모든 속성 업데이트 및 표시
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

이 명령은 파일의 모든 속성 (ACL, 사용 권한, 소유자, 그룹, 메타 데이터, 속성을 conbination으로 업데이트할 수 있음)을 업데이트 하 고 Powershell 콘솔에 표시 합니다.

### 예제 3: 디렉터리에 ACL 항목 추가
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

이 명령은 디렉터리에서 ACL을 가져오고, ACL 항목을 업데이트/추가 하 고, 디렉터리로 다시 설정 합니다.
AccessControlType/EntityId/DefaultScope가 같은 ACL 항목이 없는 경우 새 ACL 항목을 추가 하 고 기존 ACL 항목을 업데이트 합니다.

## 변수

### -Acl
파일 및 디렉터리에 대 한 POSIX 액세스 제어 권한을 설정 합니다.
새 AzDataLakeGen2ItemAclObject를 사용 하 여이 개체를 만듭니다.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -컨텍스트
Azure 저장소 컨텍스트 개체

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSystem
파일 시스템 이름

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -그룹
Blob의 소유 그룹을 설정 합니다.

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

### -InputObject
업데이트할 Azure Datalake Gen2 Item 개체

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Metadata
디렉터리 또는 파일에 대 한 메타 데이터를 지정 합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -소유자
Blob의 소유자를 설정 합니다.

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

### -Path
지정 된 파일 시스템에서 업데이트 해야 하는 경로입니다.
' Directory/file.txt ' 또는 ' directory1/directory2/' 형식의 파일 또는 디렉터리 일 수 있습니다.
이 매개 변수를 지정 하지 않으면 파일 시스템의 루트 디렉터리가 업데이트 됩니다.

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -사용 권한
파일 소유자, 소유 하는 그룹 및 다른 사용자에 대 한 POSIX 액세스 권한을 설정 합니다.
각 클래스에는 읽기, 쓰기 또는 실행 권한이 부여 될 수 있습니다.
기호 (rwxrw)가 지원 됩니다.
Acl과 함께 사용할 올바르지 않습니다.

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

### -속성
디렉터리 또는 파일의 속성을 지정 합니다. 파일에 대해 지원 되는 속성은 CacheControl, ContentDisposition, Contentdisposition, Contentdisposition, ContentMD5, ContentType입니다.
디렉터리에 대해 지원 되는 속성은 CacheControl, ContentDisposition, Contentdisposition, Contentdisposition입니다.

```yaml
Type: System.Collections.Hashtable
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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.

### Microsoft. Azure. 일반. IStorageContext

## 출력

### WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.

## 상속자

## 관련 링크
