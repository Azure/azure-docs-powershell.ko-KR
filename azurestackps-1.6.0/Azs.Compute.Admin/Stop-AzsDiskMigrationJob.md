---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522960"
---
# <span data-ttu-id="8c32f-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="8c32f-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="8c32f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c32f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c32f-103">관리 되는 디스크 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c32f-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="8c32f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c32f-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="8c32f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8c32f-105">DESCRIPTION</span></span>
<span data-ttu-id="8c32f-106">디스크 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c32f-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="8c32f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8c32f-107">EXAMPLES</span></span>

### <span data-ttu-id="8c32f-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8c32f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="8c32f-109">관리 되는 디스크 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c32f-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="8c32f-110">변수</span><span class="sxs-lookup"><span data-stu-id="8c32f-110">PARAMETERS</span></span>

### <span data-ttu-id="8c32f-111">-위치</span><span class="sxs-lookup"><span data-stu-id="8c32f-111">-Location</span></span>
<span data-ttu-id="8c32f-112">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8c32f-112">Location of the resource.</span></span>

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

### <span data-ttu-id="8c32f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="8c32f-113">-Name</span></span>
<span data-ttu-id="8c32f-114">마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c32f-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="8c32f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c32f-115">CommonParameters</span></span>
<span data-ttu-id="8c32f-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c32f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c32f-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c32f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c32f-118">입력</span><span class="sxs-lookup"><span data-stu-id="8c32f-118">INPUTS</span></span>

## <span data-ttu-id="8c32f-119">출력</span><span class="sxs-lookup"><span data-stu-id="8c32f-119">OUTPUTS</span></span>

### <span data-ttu-id="8c32f-120">DiskMigrationJob의. 관리자. 관리.</span><span class="sxs-lookup"><span data-stu-id="8c32f-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="8c32f-121">상속자</span><span class="sxs-lookup"><span data-stu-id="8c32f-121">NOTES</span></span>

## <span data-ttu-id="8c32f-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c32f-122">RELATED LINKS</span></span>

