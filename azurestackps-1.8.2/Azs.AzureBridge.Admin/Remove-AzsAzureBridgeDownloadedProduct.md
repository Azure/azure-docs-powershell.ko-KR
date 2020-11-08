---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc5311b1c26d4ae0cb9c1a7ce6ad58a818b53c6
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2020
ms.locfileid: "94215131"
---
# <span data-ttu-id="4a704-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="4a704-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="4a704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a704-102">SYNOPSIS</span></span>
<span data-ttu-id="4a704-103">Azure MarketPlace에서 다운로드 한 제품을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="4a704-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a704-104">SYNTAX</span></span>

### <span data-ttu-id="4a704-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4a704-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a704-106">리소스</span><span class="sxs-lookup"><span data-stu-id="4a704-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a704-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4a704-107">DESCRIPTION</span></span>
<span data-ttu-id="4a704-108">Azure MarketPlace에서 다운로드 한 제품을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="4a704-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4a704-109">EXAMPLES</span></span>

### <span data-ttu-id="4a704-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a704-110">EXAMPLE 1</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="4a704-111">Azure Marketplace에서 다운로드 한 제품 삭제</span><span class="sxs-lookup"><span data-stu-id="4a704-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="4a704-112">변수</span><span class="sxs-lookup"><span data-stu-id="4a704-112">PARAMETERS</span></span>

### <span data-ttu-id="4a704-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4a704-113">-Name</span></span>
<span data-ttu-id="4a704-114">제품의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-114">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a704-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="4a704-115">-ActivationName</span></span>
<span data-ttu-id="4a704-116">정품 인증의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a704-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a704-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a704-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a704-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4a704-119">-Force</span></span>
<span data-ttu-id="4a704-120">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-120">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a704-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a704-121">-ResourceId</span></span>
<span data-ttu-id="4a704-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-122">The resource id.</span></span>

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

### <span data-ttu-id="4a704-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a704-123">-AsJob</span></span>
<span data-ttu-id="4a704-124">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a704-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a704-125">-WhatIf</span></span>
<span data-ttu-id="4a704-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a704-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a704-128">-확인</span><span class="sxs-lookup"><span data-stu-id="4a704-128">-Confirm</span></span>
<span data-ttu-id="4a704-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a704-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a704-130">CommonParameters</span></span>
<span data-ttu-id="4a704-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a704-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a704-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a704-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a704-133">입력</span><span class="sxs-lookup"><span data-stu-id="4a704-133">INPUTS</span></span>

## <span data-ttu-id="4a704-134">출력</span><span class="sxs-lookup"><span data-stu-id="4a704-134">OUTPUTS</span></span>

### <span data-ttu-id="4a704-135">DownloadedProductResource. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="4a704-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="4a704-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4a704-136">NOTES</span></span>

## <span data-ttu-id="4a704-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a704-137">RELATED LINKS</span></span>
