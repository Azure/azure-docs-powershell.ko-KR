---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874694"
---
# <span data-ttu-id="dbca2-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="dbca2-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="dbca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbca2-102">SYNOPSIS</span></span>
<span data-ttu-id="dbca2-103">관리 되는 디스크 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbca2-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="dbca2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbca2-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="dbca2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbca2-105">DESCRIPTION</span></span>
<span data-ttu-id="dbca2-106">디스크 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbca2-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="dbca2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dbca2-107">EXAMPLES</span></span>

### <span data-ttu-id="dbca2-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dbca2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="dbca2-109">관리 되는 디스크 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbca2-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="dbca2-110">변수</span><span class="sxs-lookup"><span data-stu-id="dbca2-110">PARAMETERS</span></span>

### <span data-ttu-id="dbca2-111">-위치</span><span class="sxs-lookup"><span data-stu-id="dbca2-111">-Location</span></span>
<span data-ttu-id="dbca2-112">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dbca2-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbca2-113">-이름</span><span class="sxs-lookup"><span data-stu-id="dbca2-113">-Name</span></span>
<span data-ttu-id="dbca2-114">마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dbca2-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbca2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbca2-115">CommonParameters</span></span>
<span data-ttu-id="dbca2-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbca2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbca2-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbca2-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbca2-118">입력</span><span class="sxs-lookup"><span data-stu-id="dbca2-118">INPUTS</span></span>

## <span data-ttu-id="dbca2-119">출력</span><span class="sxs-lookup"><span data-stu-id="dbca2-119">OUTPUTS</span></span>

### <span data-ttu-id="dbca2-120">DiskMigrationJob의. 관리자. 관리.</span><span class="sxs-lookup"><span data-stu-id="dbca2-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="dbca2-121">상속자</span><span class="sxs-lookup"><span data-stu-id="dbca2-121">NOTES</span></span>

## <span data-ttu-id="dbca2-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbca2-122">RELATED LINKS</span></span>

