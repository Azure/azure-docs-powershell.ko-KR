---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218869"
---
# <span data-ttu-id="53dab-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="53dab-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="53dab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53dab-102">SYNOPSIS</span></span>
<span data-ttu-id="53dab-103">새 디스크 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53dab-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="53dab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53dab-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="53dab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53dab-105">DESCRIPTION</span></span>
<span data-ttu-id="53dab-106">New-AzMigrateDiskMapping cmdlet은 마이그레이션할 서버에 연결 된 원본 디스크의 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53dab-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="53dab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="53dab-107">EXAMPLES</span></span>

### <span data-ttu-id="53dab-108">예제 1: 디스크 만들기</span><span class="sxs-lookup"><span data-stu-id="53dab-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="53dab-109">디스크 개체를 다운로드 하 여 New-AzMigrateServerReplication에 대 한 입력을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="53dab-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="53dab-110">변수</span><span class="sxs-lookup"><span data-stu-id="53dab-110">PARAMETERS</span></span>

### <span data-ttu-id="53dab-111">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="53dab-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="53dab-112">사용할 디스크 encyption 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53dab-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="53dab-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="53dab-113">-DiskID</span></span>
<span data-ttu-id="53dab-114">마이그레이션할 검색 된 서버에 연결 된 디스크의 디스크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53dab-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="53dab-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="53dab-115">-DiskType</span></span>
<span data-ttu-id="53dab-116">Azure VM에 사용 되는 디스크 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53dab-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53dab-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="53dab-117">-IsOSDisk</span></span>
<span data-ttu-id="53dab-118">마이그레이션할 원본 서버에 대 한 운영 체제가 디스크에 포함 되어 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53dab-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="53dab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53dab-119">CommonParameters</span></span>
<span data-ttu-id="53dab-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53dab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53dab-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53dab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53dab-122">입력</span><span class="sxs-lookup"><span data-stu-id="53dab-122">INPUTS</span></span>

## <span data-ttu-id="53dab-123">출력</span><span class="sxs-lookup"><span data-stu-id="53dab-123">OUTPUTS</span></span>

### <span data-ttu-id="53dab-124">Api20180110. IVMwareCbtDiskInput의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="53dab-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="53dab-125">상속자</span><span class="sxs-lookup"><span data-stu-id="53dab-125">NOTES</span></span>

<span data-ttu-id="53dab-126">별칭과</span><span class="sxs-lookup"><span data-stu-id="53dab-126">ALIASES</span></span>

## <span data-ttu-id="53dab-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53dab-127">RELATED LINKS</span></span>

