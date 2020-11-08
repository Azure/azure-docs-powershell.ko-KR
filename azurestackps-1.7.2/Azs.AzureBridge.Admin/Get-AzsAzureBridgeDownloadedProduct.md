---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a9faaa3495e61186cab9d97d04e4d4b8186f152
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93883333"
---
# <span data-ttu-id="3937a-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="3937a-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="3937a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3937a-102">SYNOPSIS</span></span>
<span data-ttu-id="3937a-103">Azure MarketPlace에서 다운로드 한 제품의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="3937a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3937a-104">SYNTAX</span></span>

### <span data-ttu-id="3937a-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3937a-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3937a-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="3937a-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="3937a-107">리소스</span><span class="sxs-lookup"><span data-stu-id="3937a-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3937a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3937a-108">DESCRIPTION</span></span>
<span data-ttu-id="3937a-109">Azure MarketPlace에서 다운로드 한 제품의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="3937a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3937a-110">EXAMPLES</span></span>

### <span data-ttu-id="3937a-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3937a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="3937a-112">Azure Bridge 다운로드 제품 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="3937a-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="3937a-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3937a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="3937a-114">이름별로 다운로드 한 Azure Bridge 제품 받기</span><span class="sxs-lookup"><span data-stu-id="3937a-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="3937a-115">변수</span><span class="sxs-lookup"><span data-stu-id="3937a-115">PARAMETERS</span></span>

### <span data-ttu-id="3937a-116">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="3937a-116">-ActivationName</span></span>
<span data-ttu-id="3937a-117">정품 인증의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-117">Name of the activation.</span></span>

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

### <span data-ttu-id="3937a-118">-이름</span><span class="sxs-lookup"><span data-stu-id="3937a-118">-Name</span></span>
<span data-ttu-id="3937a-119">제품의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-119">Name of the product.</span></span>

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

### <span data-ttu-id="3937a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3937a-120">-ResourceGroupName</span></span>
<span data-ttu-id="3937a-121">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3937a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3937a-122">-ResourceId</span></span>
<span data-ttu-id="3937a-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-123">The resource id.</span></span>

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

### <span data-ttu-id="3937a-124">-생략</span><span class="sxs-lookup"><span data-stu-id="3937a-124">-Skip</span></span>
<span data-ttu-id="3937a-125">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3937a-126">-위쪽</span><span class="sxs-lookup"><span data-stu-id="3937a-126">-Top</span></span>
<span data-ttu-id="3937a-127">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3937a-128">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3937a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3937a-129">CommonParameters</span></span>
<span data-ttu-id="3937a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3937a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3937a-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3937a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3937a-132">입력</span><span class="sxs-lookup"><span data-stu-id="3937a-132">INPUTS</span></span>

## <span data-ttu-id="3937a-133">출력</span><span class="sxs-lookup"><span data-stu-id="3937a-133">OUTPUTS</span></span>

### <span data-ttu-id="3937a-134">DownloadedProductResource. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="3937a-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="3937a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="3937a-135">NOTES</span></span>

## <span data-ttu-id="3937a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3937a-136">RELATED LINKS</span></span>
