---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701697"
---
# <span data-ttu-id="740d7-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="740d7-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="740d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="740d7-102">SYNOPSIS</span></span>
<span data-ttu-id="740d7-103">현재 구독 및 지정 된 리소스 그룹 이름 아래에 있는 모든 디렉터리 테 넌 트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="740d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="740d7-104">SYNTAX</span></span>

### <span data-ttu-id="740d7-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="740d7-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="740d7-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="740d7-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="740d7-107">리소스</span><span class="sxs-lookup"><span data-stu-id="740d7-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="740d7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="740d7-108">DESCRIPTION</span></span>
<span data-ttu-id="740d7-109">현재 구독 및 지정 된 리소스 그룹 이름 아래에 있는 모든 디렉터리 테 넌 트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="740d7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="740d7-110">EXAMPLES</span></span>

### <span data-ttu-id="740d7-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="740d7-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="740d7-112">현재 구독 및 지정 된 리소스 그룹 이름 아래에 있는 모든 디렉터리 테 넌 트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="740d7-113">변수</span><span class="sxs-lookup"><span data-stu-id="740d7-113">PARAMETERS</span></span>

### <span data-ttu-id="740d7-114">-이름</span><span class="sxs-lookup"><span data-stu-id="740d7-114">-Name</span></span>
<span data-ttu-id="740d7-115">디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-115">Directory tenant name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740d7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="740d7-116">-ResourceGroupName</span></span>
<span data-ttu-id="740d7-117">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="740d7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="740d7-118">-ResourceId</span></span>
<span data-ttu-id="740d7-119">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="740d7-120">-생략</span><span class="sxs-lookup"><span data-stu-id="740d7-120">-Skip</span></span>
<span data-ttu-id="740d7-121">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740d7-122">-위쪽</span><span class="sxs-lookup"><span data-stu-id="740d7-122">-Top</span></span>
<span data-ttu-id="740d7-123">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="740d7-124">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="740d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="740d7-125">CommonParameters</span></span>
<span data-ttu-id="740d7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="740d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="740d7-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="740d7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="740d7-128">입력</span><span class="sxs-lookup"><span data-stu-id="740d7-128">INPUTS</span></span>

## <span data-ttu-id="740d7-129">출력</span><span class="sxs-lookup"><span data-stu-id="740d7-129">OUTPUTS</span></span>

### <span data-ttu-id="740d7-130">Microsoft AzureStack. 관리. DirectoryTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="740d7-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="740d7-131">상속자</span><span class="sxs-lookup"><span data-stu-id="740d7-131">NOTES</span></span>

## <span data-ttu-id="740d7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="740d7-132">RELATED LINKS</span></span>

