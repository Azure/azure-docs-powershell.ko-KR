---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcbc31b31558a38e61648a0eb9318f68daf19d2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701689"
---
# <span data-ttu-id="af31b-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="af31b-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="af31b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af31b-102">SYNOPSIS</span></span>
<span data-ttu-id="af31b-103">관리 되는 디스크 마이그레이션 작업을 시작 하 여 관리 디스크를 지정 된 대상 공유로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="af31b-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="af31b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af31b-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="af31b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="af31b-105">DESCRIPTION</span></span>
<span data-ttu-id="af31b-106">디스크 마이그레이션 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af31b-106">Create a disk migration job.</span></span>

## <span data-ttu-id="af31b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="af31b-107">EXAMPLES</span></span>

### <span data-ttu-id="af31b-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="af31b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="af31b-109">처음 20 개 디스크에 대해 관리 되는 디스크 마이그레이션 작업 시작</span><span class="sxs-lookup"><span data-stu-id="af31b-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="af31b-110">변수</span><span class="sxs-lookup"><span data-stu-id="af31b-110">PARAMETERS</span></span>

### <span data-ttu-id="af31b-111">-디스크</span><span class="sxs-lookup"><span data-stu-id="af31b-111">-Disks</span></span>
<span data-ttu-id="af31b-112">디스크 목록의 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="af31b-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31b-113">-위치</span><span class="sxs-lookup"><span data-stu-id="af31b-113">-Location</span></span>
<span data-ttu-id="af31b-114">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="af31b-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="af31b-115">-Name</span></span>
<span data-ttu-id="af31b-116">마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af31b-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31b-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="af31b-117">-TargetShare</span></span>
<span data-ttu-id="af31b-118">대상 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af31b-118">The target share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af31b-119">CommonParameters</span></span>
<span data-ttu-id="af31b-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af31b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af31b-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af31b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af31b-122">입력</span><span class="sxs-lookup"><span data-stu-id="af31b-122">INPUTS</span></span>

## <span data-ttu-id="af31b-123">출력</span><span class="sxs-lookup"><span data-stu-id="af31b-123">OUTPUTS</span></span>

### <span data-ttu-id="af31b-124">DiskMigrationJob의. 관리자. 관리.</span><span class="sxs-lookup"><span data-stu-id="af31b-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="af31b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="af31b-125">NOTES</span></span>

## <span data-ttu-id="af31b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af31b-126">RELATED LINKS</span></span>
