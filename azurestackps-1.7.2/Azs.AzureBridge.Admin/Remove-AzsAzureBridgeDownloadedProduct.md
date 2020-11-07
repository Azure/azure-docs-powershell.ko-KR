---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bde5ca1c9a354e78f04ec3c9a54da72617f7ecc5
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93883325"
---
# <span data-ttu-id="d51b1-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="d51b1-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="d51b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d51b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d51b1-103">Azure MarketPlace에서 다운로드 한 제품을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="d51b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d51b1-104">SYNTAX</span></span>

### <span data-ttu-id="d51b1-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d51b1-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d51b1-106">리소스</span><span class="sxs-lookup"><span data-stu-id="d51b1-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d51b1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d51b1-107">DESCRIPTION</span></span>
<span data-ttu-id="d51b1-108">Azure MarketPlace에서 다운로드 한 제품을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="d51b1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d51b1-109">EXAMPLES</span></span>

### <span data-ttu-id="d51b1-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d51b1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="d51b1-111">Azure Marketplace에서 다운로드 한 제품 삭제</span><span class="sxs-lookup"><span data-stu-id="d51b1-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="d51b1-112">변수</span><span class="sxs-lookup"><span data-stu-id="d51b1-112">PARAMETERS</span></span>

### <span data-ttu-id="d51b1-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="d51b1-113">-ActivationName</span></span>
<span data-ttu-id="d51b1-114">정품 인증의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-114">Name of the activation.</span></span>

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

### <span data-ttu-id="d51b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d51b1-115">-AsJob</span></span>
<span data-ttu-id="d51b1-116">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d51b1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d51b1-117">-Force</span></span>
<span data-ttu-id="d51b1-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d51b1-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d51b1-119">-Name</span></span>
<span data-ttu-id="d51b1-120">제품의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-120">Name of the product.</span></span>

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

### <span data-ttu-id="d51b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d51b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="d51b1-122">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d51b1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d51b1-123">-ResourceId</span></span>
<span data-ttu-id="d51b1-124">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-124">The resource id.</span></span>

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

### <span data-ttu-id="d51b1-125">-확인</span><span class="sxs-lookup"><span data-stu-id="d51b1-125">-Confirm</span></span>
<span data-ttu-id="d51b1-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d51b1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d51b1-127">-WhatIf</span></span>
<span data-ttu-id="d51b1-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d51b1-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d51b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51b1-130">CommonParameters</span></span>
<span data-ttu-id="d51b1-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d51b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51b1-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d51b1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51b1-133">입력</span><span class="sxs-lookup"><span data-stu-id="d51b1-133">INPUTS</span></span>

## <span data-ttu-id="d51b1-134">출력</span><span class="sxs-lookup"><span data-stu-id="d51b1-134">OUTPUTS</span></span>

### <span data-ttu-id="d51b1-135">DownloadedProductResource. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="d51b1-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="d51b1-136">상속자</span><span class="sxs-lookup"><span data-stu-id="d51b1-136">NOTES</span></span>

## <span data-ttu-id="d51b1-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d51b1-137">RELATED LINKS</span></span>

