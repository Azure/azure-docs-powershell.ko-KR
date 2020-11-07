---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cc6e2adff73e4b7c81a401bb98e9ab625005ae3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701737"
---
# <span data-ttu-id="cfb7d-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="cfb7d-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="cfb7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb7d-103">저장소 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb7d-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="cfb7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cfb7d-104">SYNTAX</span></span>

### <span data-ttu-id="cfb7d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cfb7d-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="cfb7d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="cfb7d-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="cfb7d-107">리소스</span><span class="sxs-lookup"><span data-stu-id="cfb7d-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cfb7d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cfb7d-108">DESCRIPTION</span></span>
<span data-ttu-id="cfb7d-109">저장소 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb7d-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="cfb7d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cfb7d-110">EXAMPLES</span></span>

### <span data-ttu-id="cfb7d-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cfb7d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="cfb7d-112">저장소 공유 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cfb7d-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="cfb7d-113">변수</span><span class="sxs-lookup"><span data-stu-id="cfb7d-113">PARAMETERS</span></span>

### <span data-ttu-id="cfb7d-114">-FarmName</span><span class="sxs-lookup"><span data-stu-id="cfb7d-114">-FarmName</span></span>
<span data-ttu-id="cfb7d-115">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb7d-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfb7d-116">-이름</span><span class="sxs-lookup"><span data-stu-id="cfb7d-116">-Name</span></span>
<span data-ttu-id="cfb7d-117">공유 이름.</span><span class="sxs-lookup"><span data-stu-id="cfb7d-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfb7d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfb7d-118">-ResourceGroupName</span></span>
<span data-ttu-id="cfb7d-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb7d-119">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfb7d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfb7d-120">-ResourceId</span></span>
<span data-ttu-id="cfb7d-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb7d-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfb7d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb7d-122">CommonParameters</span></span>
<span data-ttu-id="cfb7d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb7d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb7d-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfb7d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb7d-125">입력</span><span class="sxs-lookup"><span data-stu-id="cfb7d-125">INPUTS</span></span>

## <span data-ttu-id="cfb7d-126">출력</span><span class="sxs-lookup"><span data-stu-id="cfb7d-126">OUTPUTS</span></span>

### <span data-ttu-id="cfb7d-127">Microsoft AzureStack. 관리. 모델 공유</span><span class="sxs-lookup"><span data-stu-id="cfb7d-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="cfb7d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="cfb7d-128">NOTES</span></span>

## <span data-ttu-id="cfb7d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cfb7d-129">RELATED LINKS</span></span>

