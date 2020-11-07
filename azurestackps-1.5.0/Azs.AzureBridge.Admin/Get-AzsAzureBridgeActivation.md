---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 811a69b8d18c5e723702f73873188961f2739360
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93538311"
---
# <span data-ttu-id="215ad-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="215ad-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="215ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="215ad-102">SYNOPSIS</span></span>
<span data-ttu-id="215ad-103">Azure 브리지 활성화를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="215ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="215ad-104">SYNTAX</span></span>

### <span data-ttu-id="215ad-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="215ad-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="215ad-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="215ad-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="215ad-107">리소스</span><span class="sxs-lookup"><span data-stu-id="215ad-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="215ad-108">설명은</span><span class="sxs-lookup"><span data-stu-id="215ad-108">DESCRIPTION</span></span>
<span data-ttu-id="215ad-109">Azure 스택이 등록 되 면 등록 만료 날짜, 이름 등 azure의 등록에 Azure 스택 배포를 연결 하는 정보가 활성화 개체에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="215ad-110">예제의</span><span class="sxs-lookup"><span data-stu-id="215ad-110">EXAMPLES</span></span>

### <span data-ttu-id="215ad-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="215ad-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="215ad-112">리소스 그룹 "activationRG" 아래에서 Azure Bridge 정품 인증 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="215ad-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="215ad-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="215ad-114">' ActivationRG ' 아래에 있는 이름 ' myActivation '을 기준으로 Azure 브리지 활성화를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="215ad-115">변수</span><span class="sxs-lookup"><span data-stu-id="215ad-115">PARAMETERS</span></span>

### <span data-ttu-id="215ad-116">-이름</span><span class="sxs-lookup"><span data-stu-id="215ad-116">-Name</span></span>
<span data-ttu-id="215ad-117">정품 인증의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-117">Name of the activation.</span></span>

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

### <span data-ttu-id="215ad-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="215ad-118">-ResourceGroupName</span></span>
<span data-ttu-id="215ad-119">Azure 스택 등록 중에 사용 되는 리소스 그룹입니다. 포털에서 리소스 그룹 이름을 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

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

### <span data-ttu-id="215ad-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="215ad-120">-ResourceId</span></span>
<span data-ttu-id="215ad-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-121">The resource id.</span></span>

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

### <span data-ttu-id="215ad-122">-생략</span><span class="sxs-lookup"><span data-stu-id="215ad-122">-Skip</span></span>
<span data-ttu-id="215ad-123">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="215ad-124">-위쪽</span><span class="sxs-lookup"><span data-stu-id="215ad-124">-Top</span></span>
<span data-ttu-id="215ad-125">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="215ad-126">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="215ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="215ad-127">CommonParameters</span></span>
<span data-ttu-id="215ad-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="215ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="215ad-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="215ad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="215ad-130">입력</span><span class="sxs-lookup"><span data-stu-id="215ad-130">INPUTS</span></span>

## <span data-ttu-id="215ad-131">출력</span><span class="sxs-lookup"><span data-stu-id="215ad-131">OUTPUTS</span></span>

### <span data-ttu-id="215ad-132">ActivationResource. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="215ad-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="215ad-133">상속자</span><span class="sxs-lookup"><span data-stu-id="215ad-133">NOTES</span></span>

## <span data-ttu-id="215ad-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="215ad-134">RELATED LINKS</span></span>

