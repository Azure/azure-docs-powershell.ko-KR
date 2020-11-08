---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045536"
---
# <span data-ttu-id="c5638-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5638-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="c5638-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5638-102">SYNOPSIS</span></span>
<span data-ttu-id="c5638-103">Traffic Manager 프로필의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="c5638-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5638-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c5638-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c5638-105">DESCRIPTION</span></span>
<span data-ttu-id="c5638-106">**AzureTrafficManagerProfile** Cmdlet은 Microsoft Azure 트래픽 관리자 프로필의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c5638-107">*Name* 매개 변수를 지정 하지 않으면 cmdlet은 현재 구독의 Traffic Manager 프로필을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="c5638-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c5638-108">EXAMPLES</span></span>

### <span data-ttu-id="c5638-109">예제 1: 구독에서 Traffic Manager 프로필 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="c5638-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="c5638-110">이 명령은 구독에서 Traffic Manager 프로필의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="c5638-111">예제 2: Traffic Manager 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="c5638-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="c5638-112">이 명령은 MyProfile 이라는 Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="c5638-113">예제 3: Traffic Manager 프로필에 끝점 추가</span><span class="sxs-lookup"><span data-stu-id="c5638-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="c5638-114">이 명령은 Traffic Manager 프로필에 끝점을 추가한 다음 프로필을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="c5638-115">변수</span><span class="sxs-lookup"><span data-stu-id="c5638-115">PARAMETERS</span></span>

### <span data-ttu-id="c5638-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c5638-116">-Name</span></span>
<span data-ttu-id="c5638-117">가져올 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-117">Specifies the name of the Traffic Manager profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5638-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="c5638-118">-Profile</span></span>
<span data-ttu-id="c5638-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c5638-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5638-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5638-121">CommonParameters</span></span>
<span data-ttu-id="c5638-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5638-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5638-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5638-124">입력</span><span class="sxs-lookup"><span data-stu-id="c5638-124">INPUTS</span></span>

## <span data-ttu-id="c5638-125">출력</span><span class="sxs-lookup"><span data-stu-id="c5638-125">OUTPUTS</span></span>

### <span data-ttu-id="c5638-126">WindowsAzure. TrafficManager. 유틸리티. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="c5638-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="c5638-127">이 cmdlet은 Traffic Manager 프로필 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5638-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="c5638-128">상속자</span><span class="sxs-lookup"><span data-stu-id="c5638-128">NOTES</span></span>

## <span data-ttu-id="c5638-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5638-129">RELATED LINKS</span></span>

[<span data-ttu-id="c5638-130">추가-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5638-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="c5638-131">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5638-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c5638-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5638-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c5638-133">새로운 AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5638-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c5638-134">제거-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5638-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c5638-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5638-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


