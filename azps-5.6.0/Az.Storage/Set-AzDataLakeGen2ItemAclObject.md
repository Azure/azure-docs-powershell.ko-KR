---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 6396da138a0bafd54241f859c107601a1ce14b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985525"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
cmdlet에서 사용할 수 있는 DataLake gen2 항목 ACL 개체를 Update-AzDataLakeGen2Item 업데이트합니다.

## 구문

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## 설명
**Set-AzDataLakeGen2ItemAclObject** cmdlet은 dataLake gen2 항목 A Update-AzDataLakeGen2Item CL 개체를 만들고 업데이트합니다.
입력 ACL에 동일한 AccessControlType/EntityId/DefaultScope가 있는 새 ACL 항목이 없는 경우 새 ACL 항목을 만들고 기존 ACL 항목의 권한을 업데이트합니다.

## 예제

### 예제 1: ACL 항목 3개가 있는 ACL 개체 만들기 및 디렉터리에서 ACL 업데이트
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

이 명령은 ACL 항목이 3개인 ACL 개체를 만들고(-InputObject 매개 변수를 사용하여 기존 acl 개체에 acl 항목을 추가) 디렉터리에서 ACL을 업데이트합니다.

### 예제 2: ACL 항목 4개가 있는 ACL 개체 만들기 및 기존 ACL 항목의 업데이트 권한
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

이 명령은 먼저 ACL 항목이 4개인 ACL 개체를 만든 다음, 다른 사용 권한으로 cmdlet을 다시 실행하지만 기존 ACL 항목의 동일한 AccessControlType/EntityId/DefaultScope를 실행합니다.
그런 다음 ACL 항목의 사용 권한이 업데이트되지만 새 ACL 항목이 추가되지 않습니다.

## 매개 변수

### -AccessControlType
"사용자"는 소유자 또는 명명된 사용자에 대한 권한을 부여하고, "그룹"은 소유 그룹 또는 명명된 그룹에 대한 권한을 부여하며, "마스크"는 명명된 사용자 및 그룹의 구성원에게 부여된 권한을 제한하며, "기타"는 다른 항목에서 찾을 수 없는 모든 사용자에게 권한을 부여합니다.

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
ACE가 디렉터리의 기본 ACL에 속하는 것을 나타내기 위해 이 매개 변수를 설정합니다. 그렇지 않으면 범위가 암시적이며 ACE는 액세스 ACL에 속합니다.

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

### -EntityId
사용자 또는 그룹 식별자입니다.
AccessControlType "mask" 및 "other"의 항목은 생략됩니다.
사용자 또는 그룹 식별자도 소유자 및 소유 그룹에 대해 생략됩니다.

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
PSPathAccessControlEntry 개체를 입력하는 경우 \[ \] 새 ACL을 입력 PSPathAccessControlEntry 개체의 새 요소로 \[ \] 추가합니다.

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

### -권한
사용 권한 필드는 첫 번째 문자가 읽기 액세스 권한을 부여하는 'r'이고, 두 번째 문자는 쓰기 액세스 권한을 부여하는 'w'이고, 세 번째 문자는 실행 권한을 부여하는 'x'인 3자 시퀀스입니다.
액세스 권한이 부여되지 않은 경우 '-' 문자는 사용 권한이 거부된 것으로 나타 내는 데 사용됩니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry

## 참고 사항

## 관련 링크
