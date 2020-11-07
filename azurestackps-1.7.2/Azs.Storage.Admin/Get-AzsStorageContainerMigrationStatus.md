---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0207d9d2353954fc1997f5752ac6dad26dbdfa13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874456"
---
# <span data-ttu-id="54f00-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="54f00-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="54f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54f00-102">SYNOPSIS</span></span>
<span data-ttu-id="54f00-103">컨테이너 마이그레이션 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f00-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="54f00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54f00-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="54f00-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54f00-105">DESCRIPTION</span></span>
<span data-ttu-id="54f00-106">컨테이너 마이그레이션 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f00-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="54f00-107">예제의</span><span class="sxs-lookup"><span data-stu-id="54f00-107">EXAMPLES</span></span>

### <span data-ttu-id="54f00-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="54f00-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="54f00-109">컨테이너 마이그레이션 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54f00-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="54f00-110">변수</span><span class="sxs-lookup"><span data-stu-id="54f00-110">PARAMETERS</span></span>

### <span data-ttu-id="54f00-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="54f00-111">-FarmName</span></span>
<span data-ttu-id="54f00-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="54f00-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f00-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="54f00-113">-JobId</span></span>
<span data-ttu-id="54f00-114">작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="54f00-114">Operation Id.</span></span>

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

### <span data-ttu-id="54f00-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f00-115">-ResourceGroupName</span></span>
<span data-ttu-id="54f00-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54f00-116">Resource group name.</span></span>

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

### <span data-ttu-id="54f00-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f00-117">CommonParameters</span></span>
<span data-ttu-id="54f00-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54f00-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f00-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f00-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f00-120">입력</span><span class="sxs-lookup"><span data-stu-id="54f00-120">INPUTS</span></span>

## <span data-ttu-id="54f00-121">출력</span><span class="sxs-lookup"><span data-stu-id="54f00-121">OUTPUTS</span></span>

### <span data-ttu-id="54f00-122">MigrationResult. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="54f00-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="54f00-123">상속자</span><span class="sxs-lookup"><span data-stu-id="54f00-123">NOTES</span></span>

## <span data-ttu-id="54f00-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54f00-124">RELATED LINKS</span></span>

