---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d75764209b56ed0cc05d80e00581de3f982e435
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/26/2020
ms.locfileid: "94047330"
---
# <span data-ttu-id="e6e4f-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="e6e4f-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="e6e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e4f-103">Azure MarketPlace에서 다운로드 한 제품을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="e6e4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6e4f-104">SYNTAX</span></span>

### <span data-ttu-id="e6e4f-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e6e4f-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6e4f-106">리소스</span><span class="sxs-lookup"><span data-stu-id="e6e4f-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6e4f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e6e4f-107">DESCRIPTION</span></span>
<span data-ttu-id="e6e4f-108">Azure MarketPlace에서 다운로드 한 제품을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="e6e4f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e6e4f-109">EXAMPLES</span></span>

### <span data-ttu-id="e6e4f-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e6e4f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="e6e4f-111">Azure Marketplace에서 다운로드 한 제품 삭제</span><span class="sxs-lookup"><span data-stu-id="e6e4f-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="e6e4f-112">변수</span><span class="sxs-lookup"><span data-stu-id="e6e4f-112">PARAMETERS</span></span>

### <span data-ttu-id="e6e4f-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="e6e4f-113">-ActivationName</span></span>
<span data-ttu-id="e6e4f-114">정품 인증의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e4f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6e4f-115">-AsJob</span></span>
<span data-ttu-id="e6e4f-116">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e6e4f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e6e4f-117">-Force</span></span>
<span data-ttu-id="e6e4f-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e6e4f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e6e4f-119">-Name</span></span>
<span data-ttu-id="e6e4f-120">제품의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e4f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e4f-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6e4f-122">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e4f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6e4f-123">-ResourceId</span></span>
<span data-ttu-id="e6e4f-124">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-124">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e4f-125">-확인</span><span class="sxs-lookup"><span data-stu-id="e6e4f-125">-Confirm</span></span>
<span data-ttu-id="e6e4f-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e4f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e4f-127">-WhatIf</span></span>
<span data-ttu-id="e6e4f-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e4f-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e4f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e4f-130">CommonParameters</span></span>
<span data-ttu-id="e6e4f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e4f-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e4f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e4f-133">입력</span><span class="sxs-lookup"><span data-stu-id="e6e4f-133">INPUTS</span></span>

## <span data-ttu-id="e6e4f-134">출력</span><span class="sxs-lookup"><span data-stu-id="e6e4f-134">OUTPUTS</span></span>

### <span data-ttu-id="e6e4f-135">DownloadedProductResource. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="e6e4f-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="e6e4f-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e6e4f-136">NOTES</span></span>

## <span data-ttu-id="e6e4f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6e4f-137">RELATED LINKS</span></span>

