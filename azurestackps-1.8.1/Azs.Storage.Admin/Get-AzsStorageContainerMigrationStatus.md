---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875093"
---
# <span data-ttu-id="fedbc-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="fedbc-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="fedbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fedbc-102">SYNOPSIS</span></span>
<span data-ttu-id="fedbc-103">컨테이너 마이그레이션 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedbc-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="fedbc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fedbc-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fedbc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fedbc-105">DESCRIPTION</span></span>
<span data-ttu-id="fedbc-106">컨테이너 마이그레이션 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedbc-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="fedbc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fedbc-107">EXAMPLES</span></span>

### <span data-ttu-id="fedbc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fedbc-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="fedbc-109">컨테이너 마이그레이션 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fedbc-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="fedbc-110">변수</span><span class="sxs-lookup"><span data-stu-id="fedbc-110">PARAMETERS</span></span>

### <span data-ttu-id="fedbc-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="fedbc-111">-FarmName</span></span>
<span data-ttu-id="fedbc-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fedbc-112">Farm Id.</span></span>

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

### <span data-ttu-id="fedbc-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="fedbc-113">-JobId</span></span>
<span data-ttu-id="fedbc-114">작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fedbc-114">Operation Id.</span></span>

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

### <span data-ttu-id="fedbc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fedbc-115">-ResourceGroupName</span></span>
<span data-ttu-id="fedbc-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fedbc-116">Resource group name.</span></span>

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

### <span data-ttu-id="fedbc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fedbc-117">CommonParameters</span></span>
<span data-ttu-id="fedbc-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedbc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fedbc-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fedbc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fedbc-120">입력</span><span class="sxs-lookup"><span data-stu-id="fedbc-120">INPUTS</span></span>

## <span data-ttu-id="fedbc-121">출력</span><span class="sxs-lookup"><span data-stu-id="fedbc-121">OUTPUTS</span></span>

### <span data-ttu-id="fedbc-122">MigrationResult. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="fedbc-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="fedbc-123">상속자</span><span class="sxs-lookup"><span data-stu-id="fedbc-123">NOTES</span></span>

## <span data-ttu-id="fedbc-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fedbc-124">RELATED LINKS</span></span>
