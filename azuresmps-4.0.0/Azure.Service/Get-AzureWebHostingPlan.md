---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046512"
---
# <span data-ttu-id="93283-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="93283-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="93283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93283-102">SYNOPSIS</span></span>
<span data-ttu-id="93283-103">현재 구독에서 Azure 웹 호스팅 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93283-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="93283-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93283-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="93283-105">설명은</span><span class="sxs-lookup"><span data-stu-id="93283-105">DESCRIPTION</span></span>
<span data-ttu-id="93283-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="93283-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="93283-108">**AzureWebHostingPlan** cmdlet은 현재 구독에서 Azure 웹 호스팅 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93283-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="93283-109">기본적으로 **Get-AzureWebHostingPlan** 는 현재 구독의 모든 Azure 호스팅 계획을 가져오며 계획에 대 한 기본 정보를 제공 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="93283-110">*웹 공간* 및 *이름* 매개 변수를 사용 하는 경우 **Get-AzureWebHostingPlan** 는 특정 호스팅 계획 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="93283-111">현재 구독을 찾으려면 **Get-AzureSubscription** Cmdlet의 *현재* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="93283-112">현재 구독을 변경 하려면 **Select-AzureSubscription** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="93283-113">예제의</span><span class="sxs-lookup"><span data-stu-id="93283-113">EXAMPLES</span></span>

### <span data-ttu-id="93283-114">예제 1: 구독에서 모든 웹 호스팅 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="93283-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="93283-115">이 명령은 현재 구독에서 모든 Azure 웹 호스팅 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93283-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="93283-116">예제 2: 구독에서 특정 웹 호스팅 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="93283-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="93283-117">이 명령은 현재 구독의 westeuropewebspace 이라는 웹 공간에서 Default0 이라는 웹 호스팅 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93283-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="93283-118">변수</span><span class="sxs-lookup"><span data-stu-id="93283-118">PARAMETERS</span></span>

### <span data-ttu-id="93283-119">-이름</span><span class="sxs-lookup"><span data-stu-id="93283-119">-Name</span></span>
<span data-ttu-id="93283-120">구독에 대 한 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="93283-121">기본적으로이 cmdlet은 현재 구독에 있는 모든 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93283-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="93283-122">이 매개 변수는 와일드 카드 문자를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93283-122">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93283-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="93283-123">-Profile</span></span>
<span data-ttu-id="93283-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93283-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="93283-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93283-126">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="93283-126">-WebSpaceName</span></span>
<span data-ttu-id="93283-127">구독에 있는 웹 스페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="93283-128">기본적으로이 cmdlet은 지정 된 웹 공간에 있는 모든 웹 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93283-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="93283-129">이 매개 변수는 와일드 카드 문자를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93283-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93283-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93283-130">CommonParameters</span></span>
<span data-ttu-id="93283-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93283-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93283-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93283-133">입력</span><span class="sxs-lookup"><span data-stu-id="93283-133">INPUTS</span></span>

###  
<span data-ttu-id="93283-134">속성 이름으로이 cmdlet에 대 한 입력을 전달할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93283-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="93283-135">출력</span><span class="sxs-lookup"><span data-stu-id="93283-135">OUTPUTS</span></span>

### <span data-ttu-id="93283-136">WindowsAzure. WebHostingPlan에 대 한 유틸리티.</span><span class="sxs-lookup"><span data-stu-id="93283-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="93283-137">기본적으로 **Get-AzureWebHostingPlan** 는 **WebHostingPlan** 개체의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="93283-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="93283-138">상속자</span><span class="sxs-lookup"><span data-stu-id="93283-138">NOTES</span></span>

## <span data-ttu-id="93283-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93283-139">RELATED LINKS</span></span>

