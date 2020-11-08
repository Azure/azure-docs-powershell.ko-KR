---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045935"
---
# <span data-ttu-id="fa2a2-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="fa2a2-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="fa2a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2a2-103">도메인 이름을 Traffic Manager 프로필로 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="fa2a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa2a2-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fa2a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fa2a2-105">DESCRIPTION</span></span>
<span data-ttu-id="fa2a2-106">**AzureTrafficManagerDomainName** cmdlet은 도메인 이름을 Microsoft Azure Traffic Manager 프로필로 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="fa2a2-107">도메인 이름을 사용할 수 있는 경우이 cmdlet은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="fa2a2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fa2a2-108">EXAMPLES</span></span>

### <span data-ttu-id="fa2a2-109">예제 1: 도메인 이름을 사용할 수 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="fa2a2-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="fa2a2-110">이 명령은 도메인 이름 ContosoApp.trafficmanager.net을 Traffic Manager 프로필로 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="fa2a2-111">변수</span><span class="sxs-lookup"><span data-stu-id="fa2a2-111">PARAMETERS</span></span>

### <span data-ttu-id="fa2a2-112">-DomainName</span><span class="sxs-lookup"><span data-stu-id="fa2a2-112">-DomainName</span></span>
<span data-ttu-id="fa2a2-113">테스트할 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="fa2a2-114">다음 문자열을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-114">You must include the following string:</span></span> 

<span data-ttu-id="fa2a2-115">trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="fa2a2-115">.trafficmanager.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa2a2-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="fa2a2-116">-Profile</span></span>
<span data-ttu-id="fa2a2-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="fa2a2-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa2a2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2a2-119">CommonParameters</span></span>
<span data-ttu-id="fa2a2-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2a2-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa2a2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2a2-122">입력</span><span class="sxs-lookup"><span data-stu-id="fa2a2-122">INPUTS</span></span>

## <span data-ttu-id="fa2a2-123">출력</span><span class="sxs-lookup"><span data-stu-id="fa2a2-123">OUTPUTS</span></span>

### <span data-ttu-id="fa2a2-124">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fa2a2-124">System.Boolean</span></span>
<span data-ttu-id="fa2a2-125">이 cmdlet은 $True 또는 $False를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="fa2a2-126">도메인 이름을 사용할 수 있는 경우이 cmdlet은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa2a2-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="fa2a2-127">상속자</span><span class="sxs-lookup"><span data-stu-id="fa2a2-127">NOTES</span></span>

## <span data-ttu-id="fa2a2-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa2a2-128">RELATED LINKS</span></span>

