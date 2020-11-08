---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215781"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
Update-AzDataLakeGen2Item cmdlet에서 사용할 수 있는 DataLake gen2 item ACL 개체를 만들거나 업데이트 합니다.

## 구문과

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## 설명은
**AzDataLakeGen2ItemAclObject** cmdlet은 Update-AzDataLakeGen2Item cmdlet에서 사용할 수 있는 DataLake GEN2 item ACL 개체를 만들거나 업데이트 합니다.
입력 ACL에 AccessControlType/EntityId/DefaultScope가 같은 새 ACL 항목이 없는 경우 새 ACL 항목이 생성 되 고 기존 ACL 항목에 대 한 사용 권한이 업데이트 됩니다.

## 예제의

### 예제 1: ACL 항목이 3 개 있는 acl 개체를 만들고 디렉터리의 ACL을 업데이트 합니다.
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

이 명령은 ACL 항목 3 개를 사용 하 여 acl 개체를 만들고 (-InputObject 매개 변수를 사용 하 여 기존 acl 개체에 acl 항목을 추가 하 고) 디렉터리의 ACL을 업데이트 합니다.

### 예제 2: ACL 개체 4 개를 사용 하 여 엔터티를 생성 하 고 기존 ACL 항목에 대 한 업데이트 권한이 있습니다.
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

이 명령은 먼저 4 개의 ACL 항목을 사용 하 여 ACL 개체를 만든 다음, 기존 ACL 항목의 AccessControlType/EntityId/DefaultScope와 다른 권한으로 다시 cmdlet을 실행 합니다.
ACL 항목의 사용 권한이 업데이트 되지만 새 ACL 항목이 추가 되지 않습니다.

## 변수

### -AccessControlType
"사용자"는 소유자 또는 명명 된 사용자에 게 권한을 부여 하 고, "그룹"은 소유 그룹 또는 명명 된 그룹에 게 권한을 부여 하 고, "mask"는 명명 된 사용자와 그룹 구성원에 게 부여 된 권한을 제한 하 고, "기타"는 다른 항목에 없는 모든 사용자에 게 권한을 부여 합니다.

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
이 매개 변수를 설정 하 여 ACE가 디렉터리의 기본 ACL에 속함을 표시 합니다. 그렇지 않으면 범위는 암시적이 고 ACE는 액세스 ACL에 속합니다.

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
AccessControlType "mask" 및 "other"의 항목에 대해서는 생략 됩니다.
소유자 및 소유 그룹의 경우에도 사용자 또는 그룹 식별자가 생략 됩니다.

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
PSPathAccessControlEntry \[ \] 개체를 입력 하면 새 ACL이 입력 PSPathAccessControlEntry 개체의 새 요소로 추가 됩니다 \[ \] .

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

### -사용 권한
사용 권한 필드는 읽기 권한을 부여 하기 위해 첫 번째 문자가 ' r '이 고, 두 번째 문자는 쓰기 액세스 권한을 부여 하기 위한 ' w '이 고, 세 번째 문자는 ' x ' 이며 실행 권한을 부여 합니다.
액세스가 허용 되지 않는 경우 '-' 문자를 사용 하 여 사용 권한이 거부 되었음을 나타냅니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### WindowsAzure. ResourceModel를 PSPathAccessControlEntry로 저장 합니다.

## 상속자

## 관련 링크
