---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046415"
---
# <span data-ttu-id="7d3be-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="7d3be-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="7d3be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d3be-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3be-103">기존 추가 기능 인스턴스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="7d3be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d3be-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7d3be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7d3be-105">DESCRIPTION</span></span>
<span data-ttu-id="7d3be-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7d3be-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7d3be-108">이 cmdlet은 현재 구독에서 기존 추가 기능 인스턴스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="7d3be-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7d3be-109">EXAMPLES</span></span>

### <span data-ttu-id="7d3be-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d3be-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="7d3be-111">이 예제에서는 새 계획 ID를 사용 하 여 추가 기능을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="7d3be-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7d3be-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="7d3be-113">이 예제에서는 새 계획 ID 및 홍보 코드를 사용 하 여 추가 기능을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="7d3be-114">변수</span><span class="sxs-lookup"><span data-stu-id="7d3be-114">PARAMETERS</span></span>

### <span data-ttu-id="7d3be-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7d3be-115">-Name</span></span>
<span data-ttu-id="7d3be-116">추가 기능 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="7d3be-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d3be-117">-PassThru</span></span>
<span data-ttu-id="7d3be-118">지정 하는 경우, 명령이 성공한 경우 cmdlet은 true를 반환 하 고 실패할 경우 false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3be-119">-계획</span><span class="sxs-lookup"><span data-stu-id="7d3be-119">-Plan</span></span>
<span data-ttu-id="7d3be-120">계획 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="7d3be-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="7d3be-121">-Profile</span></span>
<span data-ttu-id="7d3be-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d3be-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d3be-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="7d3be-124">-PromotionCode</span></span>
<span data-ttu-id="7d3be-125">홍보 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-125">Specifies the promotional code.</span></span>

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

### <span data-ttu-id="7d3be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3be-126">CommonParameters</span></span>
<span data-ttu-id="7d3be-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d3be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3be-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d3be-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3be-129">입력</span><span class="sxs-lookup"><span data-stu-id="7d3be-129">INPUTS</span></span>

## <span data-ttu-id="7d3be-130">출력</span><span class="sxs-lookup"><span data-stu-id="7d3be-130">OUTPUTS</span></span>

## <span data-ttu-id="7d3be-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7d3be-131">NOTES</span></span>

## <span data-ttu-id="7d3be-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d3be-132">RELATED LINKS</span></span>

[<span data-ttu-id="7d3be-133">Get-Azure프로젝트 추가 기능</span><span class="sxs-lookup"><span data-stu-id="7d3be-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="7d3be-134">새-Azure추가 기능</span><span class="sxs-lookup"><span data-stu-id="7d3be-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="7d3be-135">-Azure추가 기능 제거</span><span class="sxs-lookup"><span data-stu-id="7d3be-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)


