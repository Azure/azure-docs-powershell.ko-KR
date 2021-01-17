---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348369"
---
# <span data-ttu-id="ae032-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="ae032-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="ae032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae032-102">SYNOPSIS</span></span>
<span data-ttu-id="ae032-103">DataLake gen2 항목 ACL 개체를 만들고 업데이트합니다. 이 개체는 Update-AzDataLakeGen2Item cmdlet에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="ae032-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae032-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="ae032-105">설명</span><span class="sxs-lookup"><span data-stu-id="ae032-105">DESCRIPTION</span></span>
<span data-ttu-id="ae032-106">**Set-AzDataLakeGen2ItemAclObject** cmdlet은 Update-AzDataLakeGen2Item cmdlet에 사용할 수 있는 DataLake gen2 항목 ACL 개체를 만들고 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="ae032-107">동일한 AccessControlType/EntityId/DefaultScope가 있는 새 ACL 항목이 입력 ACL에 없는 경우 새 ACL 항목을 만들고, 그렇지 않은 경우 기존 ACL 항목의 업데이트 권한을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="ae032-108">예제</span><span class="sxs-lookup"><span data-stu-id="ae032-108">EXAMPLES</span></span>

### <span data-ttu-id="ae032-109">예제 1: 3개 ACL 항목이 있는 ACL 개체 만들기 및 디렉터리에서 ACL 업데이트</span><span class="sxs-lookup"><span data-stu-id="ae032-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="ae032-110">이 명령은 3개 ACL 항목(-InputObject 매개 변수를 사용하여 기존 acl 개체에 acl 항목 추가)이 있는 ACL 개체를 만들고 디렉터리에서 ACL을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="ae032-111">예제 2: 4개 ACL 항목이 있는 ACL 개체 만들기 및 기존 ACL 항목의 업데이트 권한</span><span class="sxs-lookup"><span data-stu-id="ae032-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="ae032-112">이 명령은 먼저 4개 ACL 항목으로 ACL 개체를 만든 다음, 다른 사용 권한은 있지만 기존 ACL 항목의 AccessControlType/EntityId/DefaultScope와 동일한 cmdlet을 다시 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="ae032-113">그런 다음 ACL 항목의 사용 권한이 업데이트되지만 새 ACL 항목이 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="ae032-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae032-114">PARAMETERS</span></span>

### <span data-ttu-id="ae032-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="ae032-115">-AccessControlType</span></span>
<span data-ttu-id="ae032-116">"사용자"는 소유자 또는 명명된 사용자에게 권한을 부여하고, "그룹"은 소유 그룹 또는 명명된 그룹에 대한 권한을 부여하고, "마스크"는 명명된 사용자 및 그룹의 구성원에게 부여된 권한을 제한하며, "기타"는 다른 항목에 없는 모든 사용자에게 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="ae032-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="ae032-117">-DefaultScope</span></span>
<span data-ttu-id="ae032-118">ACE가 디렉터리에 대한 기본 ACL에 속해 있는 것을 나타내기 위해 이 매개 변수를 설정합니다. 그렇지 않으면 범위가 암시적이고 ACE는 액세스 ACL에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="ae032-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="ae032-119">-EntityId</span></span>
<span data-ttu-id="ae032-120">사용자 또는 그룹 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-120">The user or group identifier.</span></span>
<span data-ttu-id="ae032-121">AccessControlType "mask" 및 "other"의 항목에는 생략됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="ae032-122">소유자 및 소유 그룹에 대한 사용자 또는 그룹 식별자도 생략됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="ae032-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae032-123">-InputObject</span></span>
<span data-ttu-id="ae032-124">PSPathAccessControlEntry 개체를 입력하는 경우 새 \[ \] ACL을 PSPathAccessControlEntry 개체 입력의 새 요소로 \[ \] 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="ae032-125">-Permission</span><span class="sxs-lookup"><span data-stu-id="ae032-125">-Permission</span></span>
<span data-ttu-id="ae032-126">사용 권한 필드는 첫 번째 문자가 읽기 액세스 권한을 부여하는 'r'이고, 두 번째 문자는 쓰기 액세스 권한을 부여하는 'w'이고, 세 번째 문자는 실행 권한을 부여하는 'x'인 3자 시퀀스입니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="ae032-127">액세스 권한이 부여되지 않은 경우 '-' 문자는 사용 권한이 거부된 것으로 나타 내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="ae032-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae032-128">CommonParameters</span></span>
<span data-ttu-id="ae032-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae032-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae032-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ae032-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae032-131">입력</span><span class="sxs-lookup"><span data-stu-id="ae032-131">INPUTS</span></span>

### <span data-ttu-id="ae032-132">없음</span><span class="sxs-lookup"><span data-stu-id="ae032-132">None</span></span>

## <span data-ttu-id="ae032-133">출력</span><span class="sxs-lookup"><span data-stu-id="ae032-133">OUTPUTS</span></span>

### <span data-ttu-id="ae032-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="ae032-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="ae032-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae032-135">NOTES</span></span>

## <span data-ttu-id="ae032-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae032-136">RELATED LINKS</span></span>
