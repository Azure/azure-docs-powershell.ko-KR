---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698388"
---
# <span data-ttu-id="d2283-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d2283-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="d2283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2283-102">SYNOPSIS</span></span>
<span data-ttu-id="d2283-103">로컬 트래픽 관리자 프로필 개체에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="d2283-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2283-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2283-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d2283-105">DESCRIPTION</span></span>
<span data-ttu-id="d2283-106">**AzTrafficManagerEndpointConfig** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="d2283-107">Get-AzTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="d2283-108">이 cmdlet은 로컬 프로필 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="d2283-109">Set-AzTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="d2283-110">한 번의 작업으로 끝점을 제거 하 고 변경 내용을 커밋하려면 Remove-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="d2283-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d2283-111">EXAMPLES</span></span>

### <span data-ttu-id="d2283-112">예제 1: 끝점 제거</span><span class="sxs-lookup"><span data-stu-id="d2283-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="d2283-113">첫 번째 명령은 **AzTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="d2283-114">명령은 로컬 프로필을 $TrafficManagerProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="d2283-115">두 번째 명령은 $TrafficManagerProfile에 저장 된 프로필에서 contoso 라는 Azure 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="d2283-116">이 명령은 로컬 개체만 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-116">This command changes only the local object.</span></span>

<span data-ttu-id="d2283-117">마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 ContosoProfile 이라는 Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="d2283-118">변수</span><span class="sxs-lookup"><span data-stu-id="d2283-118">PARAMETERS</span></span>

### <span data-ttu-id="d2283-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2283-119">-DefaultProfile</span></span>
<span data-ttu-id="d2283-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2283-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d2283-121">-EndpointName</span></span>
<span data-ttu-id="d2283-122">이 cmdlet이 제거 하는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2283-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d2283-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="d2283-124">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="d2283-125">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="d2283-126">**TrafficManagerProfile** 개체를 가져오려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2283-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2283-127">CommonParameters</span></span>
<span data-ttu-id="d2283-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2283-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2283-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2283-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2283-130">입력</span><span class="sxs-lookup"><span data-stu-id="d2283-130">INPUTS</span></span>

### <span data-ttu-id="d2283-131">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="d2283-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d2283-132">출력</span><span class="sxs-lookup"><span data-stu-id="d2283-132">OUTPUTS</span></span>

### <span data-ttu-id="d2283-133">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="d2283-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d2283-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d2283-134">NOTES</span></span>

## <span data-ttu-id="d2283-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2283-135">RELATED LINKS</span></span>

[<span data-ttu-id="d2283-136">추가-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d2283-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="d2283-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d2283-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d2283-138">제거-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2283-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d2283-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d2283-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

