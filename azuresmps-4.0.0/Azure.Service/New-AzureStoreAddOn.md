---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046201"
---
# <span data-ttu-id="506c5-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="506c5-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="506c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="506c5-102">SYNOPSIS</span></span>
<span data-ttu-id="506c5-103">새 추가 기능 인스턴스를 구입 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="506c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="506c5-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="506c5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="506c5-105">DESCRIPTION</span></span>
<span data-ttu-id="506c5-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="506c5-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="506c5-108">Azure Store에서 새 추가 기능 인스턴스를 구입 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="506c5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="506c5-109">EXAMPLES</span></span>

### <span data-ttu-id="506c5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="506c5-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="506c5-111">이 예제에서는 MyAddOn 이라는 추가 기능을 구입 하 여 PlanId의 US 위치에 있는 사용자와 함께 구매 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="506c5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="506c5-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="506c5-113">이 예제에서는 홍보 코드를 사용 하 여 추가 기능을 구입 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="506c5-114">변수</span><span class="sxs-lookup"><span data-stu-id="506c5-114">PARAMETERS</span></span>

### <span data-ttu-id="506c5-115">-AddOn</span><span class="sxs-lookup"><span data-stu-id="506c5-115">-AddOn</span></span>
<span data-ttu-id="506c5-116">추가 기능 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-116">Specifies the add-on ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="506c5-117">-위치</span><span class="sxs-lookup"><span data-stu-id="506c5-117">-Location</span></span>
<span data-ttu-id="506c5-118">추가 기능 인스턴스 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-118">Specifies the add-on instance location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="506c5-119">-이름</span><span class="sxs-lookup"><span data-stu-id="506c5-119">-Name</span></span>
<span data-ttu-id="506c5-120">추가 기능 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-120">Specifies the name of the add-on instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="506c5-121">-계획</span><span class="sxs-lookup"><span data-stu-id="506c5-121">-Plan</span></span>
<span data-ttu-id="506c5-122">계획 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-122">Specifies the plan ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="506c5-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="506c5-123">-Profile</span></span>
<span data-ttu-id="506c5-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="506c5-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="506c5-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="506c5-126">-PromotionCode</span></span>
<span data-ttu-id="506c5-127">구매에 적용할 프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-127">Specifies a promotion code to apply to the purchase.</span></span>

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

### <span data-ttu-id="506c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506c5-128">CommonParameters</span></span>
<span data-ttu-id="506c5-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="506c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506c5-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="506c5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506c5-131">입력</span><span class="sxs-lookup"><span data-stu-id="506c5-131">INPUTS</span></span>

## <span data-ttu-id="506c5-132">출력</span><span class="sxs-lookup"><span data-stu-id="506c5-132">OUTPUTS</span></span>

## <span data-ttu-id="506c5-133">상속자</span><span class="sxs-lookup"><span data-stu-id="506c5-133">NOTES</span></span>

## <span data-ttu-id="506c5-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="506c5-134">RELATED LINKS</span></span>

[<span data-ttu-id="506c5-135">Get-Azure프로젝트 추가 기능</span><span class="sxs-lookup"><span data-stu-id="506c5-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="506c5-136">-Azure추가 기능 제거</span><span class="sxs-lookup"><span data-stu-id="506c5-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="506c5-137">Set-Azure기능 추가 기능</span><span class="sxs-lookup"><span data-stu-id="506c5-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


