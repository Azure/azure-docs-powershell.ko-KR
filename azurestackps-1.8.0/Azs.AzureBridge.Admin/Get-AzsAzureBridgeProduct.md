---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c875b28f6518a836296fe1f5f19910d549b880c7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93883301"
---
# <span data-ttu-id="13ad4-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="13ad4-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="13ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="13ad4-103">Azure Marketplace에서 다운로드할 수 있는 제품 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="13ad4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13ad4-104">SYNTAX</span></span>

### <span data-ttu-id="13ad4-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="13ad4-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="13ad4-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="13ad4-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="13ad4-107">리소스</span><span class="sxs-lookup"><span data-stu-id="13ad4-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="13ad4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="13ad4-108">DESCRIPTION</span></span>
<span data-ttu-id="13ad4-109">Azure Marketplace에서 다운로드할 수 있는 제품 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="13ad4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="13ad4-110">EXAMPLES</span></span>

### <span data-ttu-id="13ad4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="13ad4-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="13ad4-112">Azure Marketplace에서 다운로드할 수 있는 제품 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="13ad4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="13ad4-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="13ad4-114">Azure Marketplace에서 이름으로 다운로드 하는 데 사용할 수 있는 제품 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="13ad4-115">변수</span><span class="sxs-lookup"><span data-stu-id="13ad4-115">PARAMETERS</span></span>

### <span data-ttu-id="13ad4-116">-이름</span><span class="sxs-lookup"><span data-stu-id="13ad4-116">-Name</span></span>
<span data-ttu-id="13ad4-117">제품의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-117">Name of the product.</span></span>

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

### <span data-ttu-id="13ad4-118">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="13ad4-118">-ActivationName</span></span>
<span data-ttu-id="13ad4-119">정품 인증의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-119">Name of the activation.</span></span>

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

### <span data-ttu-id="13ad4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ad4-120">-ResourceGroupName</span></span>
<span data-ttu-id="13ad4-121">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="13ad4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13ad4-122">-ResourceId</span></span>
<span data-ttu-id="13ad4-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-123">The resource id.</span></span>

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

### <span data-ttu-id="13ad4-124">-생략</span><span class="sxs-lookup"><span data-stu-id="13ad4-124">-Skip</span></span>
<span data-ttu-id="13ad4-125">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="13ad4-126">-위쪽</span><span class="sxs-lookup"><span data-stu-id="13ad4-126">-Top</span></span>
<span data-ttu-id="13ad4-127">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="13ad4-128">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="13ad4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ad4-129">CommonParameters</span></span>
<span data-ttu-id="13ad4-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13ad4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ad4-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ad4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ad4-132">입력</span><span class="sxs-lookup"><span data-stu-id="13ad4-132">INPUTS</span></span>

## <span data-ttu-id="13ad4-133">출력</span><span class="sxs-lookup"><span data-stu-id="13ad4-133">OUTPUTS</span></span>

### <span data-ttu-id="13ad4-134">. Azurestack. 관리자. 제품 리소스</span><span class="sxs-lookup"><span data-stu-id="13ad4-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="13ad4-135">상속자</span><span class="sxs-lookup"><span data-stu-id="13ad4-135">NOTES</span></span>

## <span data-ttu-id="13ad4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13ad4-136">RELATED LINKS</span></span>
