---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034689"
---
# <span data-ttu-id="34fea-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="34fea-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="34fea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34fea-102">SYNOPSIS</span></span>
<span data-ttu-id="34fea-103">Update-AzDataLakeGen2Item cmdlet에서 사용할 수 있는 DataLake gen2 item ACL 개체를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="34fea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34fea-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="34fea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34fea-105">DESCRIPTION</span></span>
<span data-ttu-id="34fea-106">**AzDataLakeGen2ItemAclObject** cmdlet은 Update-AzDataLakeGen2Item cmdlet에서 사용할 수 있는 DataLake GEN2 item ACL 개체를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="34fea-107">입력 ACL에 AccessControlType/EntityId/DefaultScope가 같은 새 ACL 항목이 없는 경우 새 ACL 항목이 생성 되 고 기존 ACL 항목에 대 한 사용 권한이 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="34fea-108">예제의</span><span class="sxs-lookup"><span data-stu-id="34fea-108">EXAMPLES</span></span>

### <span data-ttu-id="34fea-109">예제 1: ACL 항목이 3 개 있는 acl 개체를 만들고 디렉터리의 ACL을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="34fea-110">이 명령은 ACL 항목 3 개를 사용 하 여 acl 개체를 만들고 (-InputObject 매개 변수를 사용 하 여 기존 acl 개체에 acl 항목을 추가 하 고) 디렉터리의 ACL을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="34fea-111">예제 2: ACL 개체 4 개를 사용 하 여 엔터티를 생성 하 고 기존 ACL 항목에 대 한 업데이트 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="34fea-112">이 명령은 먼저 4 개의 ACL 항목을 사용 하 여 ACL 개체를 만든 다음, 기존 ACL 항목의 AccessControlType/EntityId/DefaultScope와 다른 권한으로 다시 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="34fea-113">ACL 항목의 사용 권한이 업데이트 되지만 새 ACL 항목이 추가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="34fea-114">변수</span><span class="sxs-lookup"><span data-stu-id="34fea-114">PARAMETERS</span></span>

### <span data-ttu-id="34fea-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="34fea-115">-AccessControlType</span></span>
<span data-ttu-id="34fea-116">"사용자"는 소유자 또는 명명 된 사용자에 게 권한을 부여 하 고, "그룹"은 소유 그룹 또는 명명 된 그룹에 게 권한을 부여 하 고, "mask"는 명명 된 사용자와 그룹 구성원에 게 부여 된 권한을 제한 하 고, "기타"는 다른 항목에 없는 모든 사용자에 게 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="34fea-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="34fea-117">-DefaultScope</span></span>
<span data-ttu-id="34fea-118">이 매개 변수를 설정 하 여 ACE가 디렉터리의 기본 ACL에 속함을 표시 합니다. 그렇지 않으면 범위는 암시적이 고 ACE는 액세스 ACL에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="34fea-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="34fea-119">-EntityId</span></span>
<span data-ttu-id="34fea-120">사용자 또는 그룹 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-120">The user or group identifier.</span></span>
<span data-ttu-id="34fea-121">AccessControlType "mask" 및 "other"의 항목에 대해서는 생략 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="34fea-122">소유자 및 소유 그룹의 경우에도 사용자 또는 그룹 식별자가 생략 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="34fea-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34fea-123">-InputObject</span></span>
<span data-ttu-id="34fea-124">PSPathAccessControlEntry \[ \] 개체를 입력 하면 새 ACL이 입력 PSPathAccessControlEntry 개체의 새 요소로 추가 됩니다 \[ \] .</span><span class="sxs-lookup"><span data-stu-id="34fea-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="34fea-125">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="34fea-125">-Permission</span></span>
<span data-ttu-id="34fea-126">사용 권한 필드는 읽기 권한을 부여 하기 위해 첫 번째 문자가 ' r '이 고, 두 번째 문자는 쓰기 액세스 권한을 부여 하기 위한 ' w '이 고, 세 번째 문자는 ' x ' 이며 실행 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="34fea-127">액세스가 허용 되지 않는 경우 '-' 문자를 사용 하 여 사용 권한이 거부 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="34fea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34fea-128">CommonParameters</span></span>
<span data-ttu-id="34fea-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34fea-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34fea-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34fea-131">입력</span><span class="sxs-lookup"><span data-stu-id="34fea-131">INPUTS</span></span>

### <span data-ttu-id="34fea-132">않아야</span><span class="sxs-lookup"><span data-stu-id="34fea-132">None</span></span>

## <span data-ttu-id="34fea-133">출력</span><span class="sxs-lookup"><span data-stu-id="34fea-133">OUTPUTS</span></span>

### <span data-ttu-id="34fea-134">WindowsAzure. ResourceModel를 PSPathAccessControlEntry로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="34fea-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="34fea-135">상속자</span><span class="sxs-lookup"><span data-stu-id="34fea-135">NOTES</span></span>

## <span data-ttu-id="34fea-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34fea-136">RELATED LINKS</span></span>
