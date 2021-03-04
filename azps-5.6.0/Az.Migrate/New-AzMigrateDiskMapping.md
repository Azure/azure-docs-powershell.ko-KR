---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 1fc58ff016c41e693c059ce792a8dc8aa06e0d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982779"
---
# <span data-ttu-id="fe81a-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="fe81a-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="fe81a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe81a-102">SYNOPSIS</span></span>
<span data-ttu-id="fe81a-103">새 디스크 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe81a-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="fe81a-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe81a-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <String> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="fe81a-105">설명</span><span class="sxs-lookup"><span data-stu-id="fe81a-105">DESCRIPTION</span></span>
<span data-ttu-id="fe81a-106">New-AzMigrateDiskMapping cmdlet은 마이그레이션할 서버에 연결된 원본 디스크의 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe81a-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="fe81a-107">예제</span><span class="sxs-lookup"><span data-stu-id="fe81a-107">EXAMPLES</span></span>

### <span data-ttu-id="fe81a-108">예제 1: 디스크 만들기</span><span class="sxs-lookup"><span data-stu-id="fe81a-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="fe81a-109">디스크 개체를 사용하여 디스크에 대한 입력을 New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="fe81a-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="fe81a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fe81a-110">PARAMETERS</span></span>

### <span data-ttu-id="fe81a-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="fe81a-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="fe81a-112">사용할 디스크 encyption 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe81a-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="fe81a-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="fe81a-113">-DiskID</span></span>
<span data-ttu-id="fe81a-114">마이그레이션할 검색된 서버에 연결된 디스크의 디스크 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe81a-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="fe81a-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="fe81a-115">-DiskType</span></span>
<span data-ttu-id="fe81a-116">Azure VM에 사용할 디스크 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe81a-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="fe81a-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="fe81a-117">-IsOSDisk</span></span>
<span data-ttu-id="fe81a-118">디스크에 마이그레이션할 원본 서버에 대한 운영 체제가 포함되어 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe81a-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="fe81a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe81a-119">CommonParameters</span></span>
<span data-ttu-id="fe81a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe81a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe81a-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe81a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe81a-122">입력</span><span class="sxs-lookup"><span data-stu-id="fe81a-122">INPUTS</span></span>

## <span data-ttu-id="fe81a-123">출력</span><span class="sxs-lookup"><span data-stu-id="fe81a-123">OUTPUTS</span></span>

### <span data-ttu-id="fe81a-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="fe81a-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="fe81a-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe81a-125">NOTES</span></span>

<span data-ttu-id="fe81a-126">별칭</span><span class="sxs-lookup"><span data-stu-id="fe81a-126">ALIASES</span></span>

## <span data-ttu-id="fe81a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe81a-127">RELATED LINKS</span></span>

