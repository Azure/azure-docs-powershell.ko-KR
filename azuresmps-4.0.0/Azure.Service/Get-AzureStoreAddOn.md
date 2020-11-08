---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045547"
---
# <span data-ttu-id="37bb4-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="37bb4-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="37bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="37bb4-103">사용할 수 있는 Azure Store 추가 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="37bb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37bb4-104">SYNTAX</span></span>

### <span data-ttu-id="37bb4-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="37bb4-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="37bb4-106">GetAddOn</span><span class="sxs-lookup"><span data-stu-id="37bb4-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37bb4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="37bb4-107">DESCRIPTION</span></span>
<span data-ttu-id="37bb4-108">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="37bb4-109">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="37bb4-110">Azure Store에서 구입 하는 데 사용할 수 있는 추가 기능을 모두 가져오거나 현재 구독에 대 한 기존 추가 기능 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="37bb4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="37bb4-111">EXAMPLES</span></span>

### <span data-ttu-id="37bb4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="37bb4-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="37bb4-113">이 예제에서는 현재 구독에 대해 구매한 모든 추가 기능 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="37bb4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="37bb4-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="37bb4-115">이 예제에서는 Azure Store에서 미국에서 구매할 수 있는 모든 추가 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="37bb4-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="37bb4-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="37bb4-117">이 예제에서는 현재 구독의 구매한 추가 기능 인스턴스에서 MyAddOn 이라는 추가 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="37bb4-118">변수</span><span class="sxs-lookup"><span data-stu-id="37bb4-118">PARAMETERS</span></span>

### <span data-ttu-id="37bb4-119">-국가</span><span class="sxs-lookup"><span data-stu-id="37bb4-119">-Country</span></span>
<span data-ttu-id="37bb4-120">지정 된 경우 지정 된 국가에서 사용 가능한 Azure Store 추가 기능 인스턴스만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="37bb4-121">기본값은 "US"입니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37bb4-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="37bb4-122">-ListAvailable</span></span>
<span data-ttu-id="37bb4-123">지정 하는 경우 Azure Store에서 구매할 수 있는 추가 기능을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37bb4-124">-이름</span><span class="sxs-lookup"><span data-stu-id="37bb4-124">-Name</span></span>
<span data-ttu-id="37bb4-125">지정 된 이름과 일치 하는 추가 기능을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37bb4-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="37bb4-126">-Profile</span></span>
<span data-ttu-id="37bb4-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37bb4-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37bb4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37bb4-129">CommonParameters</span></span>
<span data-ttu-id="37bb4-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37bb4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37bb4-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37bb4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37bb4-132">입력</span><span class="sxs-lookup"><span data-stu-id="37bb4-132">INPUTS</span></span>

## <span data-ttu-id="37bb4-133">출력</span><span class="sxs-lookup"><span data-stu-id="37bb4-133">OUTPUTS</span></span>

## <span data-ttu-id="37bb4-134">상속자</span><span class="sxs-lookup"><span data-stu-id="37bb4-134">NOTES</span></span>

## <span data-ttu-id="37bb4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37bb4-135">RELATED LINKS</span></span>

[<span data-ttu-id="37bb4-136">새-Azure추가 기능</span><span class="sxs-lookup"><span data-stu-id="37bb4-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="37bb4-137">-Azure추가 기능 제거</span><span class="sxs-lookup"><span data-stu-id="37bb4-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="37bb4-138">Set-Azure기능 추가 기능</span><span class="sxs-lookup"><span data-stu-id="37bb4-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


