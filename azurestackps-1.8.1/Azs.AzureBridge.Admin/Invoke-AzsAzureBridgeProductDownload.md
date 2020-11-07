---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 107709fa7431e8c37f156f1304f560e42c08ed60
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93883354"
---
# <span data-ttu-id="61bdc-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="61bdc-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="61bdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="61bdc-103">Azure marketplace에서 제품을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="61bdc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61bdc-104">SYNTAX</span></span>

### <span data-ttu-id="61bdc-105">Products_Download (기본값)</span><span class="sxs-lookup"><span data-stu-id="61bdc-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61bdc-106">리소스</span><span class="sxs-lookup"><span data-stu-id="61bdc-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61bdc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="61bdc-107">DESCRIPTION</span></span>
<span data-ttu-id="61bdc-108">Azure marketplace에서 제품을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="61bdc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="61bdc-109">EXAMPLES</span></span>

### <span data-ttu-id="61bdc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="61bdc-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="61bdc-111">Azure Marketplace에서 제품 다운로드</span><span class="sxs-lookup"><span data-stu-id="61bdc-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="61bdc-112">변수</span><span class="sxs-lookup"><span data-stu-id="61bdc-112">PARAMETERS</span></span>

### <span data-ttu-id="61bdc-113">-이름</span><span class="sxs-lookup"><span data-stu-id="61bdc-113">-Name</span></span>
<span data-ttu-id="61bdc-114">제품 이름</span><span class="sxs-lookup"><span data-stu-id="61bdc-114">Name of the product</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bdc-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="61bdc-115">-ActivationName</span></span>
<span data-ttu-id="61bdc-116">정품 인증의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bdc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bdc-117">-ResourceGroupName</span></span>
<span data-ttu-id="61bdc-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bdc-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61bdc-119">-ResourceId</span></span>
<span data-ttu-id="61bdc-120">Azure bridge 제품의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-120">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="61bdc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61bdc-121">-AsJob</span></span>
<span data-ttu-id="61bdc-122">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-122">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="61bdc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="61bdc-123">-Force</span></span>
<span data-ttu-id="61bdc-124">스위치 매개 변수를 확인 하 라는 메시지가 표시 되지 않음</span><span class="sxs-lookup"><span data-stu-id="61bdc-124">Switch parameter not to ask for confirmation</span></span>

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

### <span data-ttu-id="61bdc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bdc-125">-WhatIf</span></span>
<span data-ttu-id="61bdc-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61bdc-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bdc-128">-확인</span><span class="sxs-lookup"><span data-stu-id="61bdc-128">-Confirm</span></span>
<span data-ttu-id="61bdc-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bdc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bdc-130">CommonParameters</span></span>
<span data-ttu-id="61bdc-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61bdc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bdc-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61bdc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bdc-133">입력</span><span class="sxs-lookup"><span data-stu-id="61bdc-133">INPUTS</span></span>

## <span data-ttu-id="61bdc-134">출력</span><span class="sxs-lookup"><span data-stu-id="61bdc-134">OUTPUTS</span></span>

## <span data-ttu-id="61bdc-135">상속자</span><span class="sxs-lookup"><span data-stu-id="61bdc-135">NOTES</span></span>

## <span data-ttu-id="61bdc-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61bdc-136">RELATED LINKS</span></span>
