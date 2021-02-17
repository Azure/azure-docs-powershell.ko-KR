---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190532"
---
# <span data-ttu-id="b8a28-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b8a28-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="b8a28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a28-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a28-103">로컬 Traffic Manager 프로필 개체에서 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="b8a28-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8a28-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a28-105">설명</span><span class="sxs-lookup"><span data-stu-id="b8a28-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a28-106">**Remove-AzTrafficManagerEndpointConfig** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에서 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="b8a28-107">Get-AzTrafficManagerProfile cmdlet을 사용하여 프로필을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="b8a28-108">이 cmdlet은 로컬 프로필 개체에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="b8a28-109">Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager에 대한 프로필에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b8a28-110">엔드포인트를 제거하고 단일 작업에서 변경 내용을 커밋하려면 Remove-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="b8a28-111">예제</span><span class="sxs-lookup"><span data-stu-id="b8a28-111">EXAMPLES</span></span>

### <span data-ttu-id="b8a28-112">예제 1: 엔드포인트 제거</span><span class="sxs-lookup"><span data-stu-id="b8a28-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b8a28-113">첫 번째 명령은 **Get-AzTrafficManagerProfile** cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="b8a28-114">이 명령은 로컬 프로필을 $TrafficManagerProfile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b8a28-115">두 번째 명령은 azure에 저장된 프로필에서 contoso라는 Azure 엔드포인트를 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b8a28-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b8a28-116">이 명령은 로컬 개체만 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-116">This command changes only the local object.</span></span>

<span data-ttu-id="b8a28-117">마지막 명령은 ContosoProfile이라는 Traffic Manager 프로필을 업데이트하여 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b8a28-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b8a28-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8a28-118">PARAMETERS</span></span>

### <span data-ttu-id="b8a28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a28-119">-DefaultProfile</span></span>
<span data-ttu-id="b8a28-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8a28-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b8a28-121">-EndpointName</span></span>
<span data-ttu-id="b8a28-122">이 cmdlet에서 제거하는 Traffic Manager 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b8a28-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8a28-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="b8a28-124">로컬 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b8a28-125">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b8a28-126">**TrafficManagerProfile** 개체를 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b8a28-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a28-127">CommonParameters</span></span>
<span data-ttu-id="b8a28-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a28-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a28-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b8a28-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a28-130">입력</span><span class="sxs-lookup"><span data-stu-id="b8a28-130">INPUTS</span></span>

### <span data-ttu-id="b8a28-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8a28-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b8a28-132">출력</span><span class="sxs-lookup"><span data-stu-id="b8a28-132">OUTPUTS</span></span>

### <span data-ttu-id="b8a28-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8a28-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b8a28-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8a28-134">NOTES</span></span>

## <span data-ttu-id="b8a28-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8a28-135">RELATED LINKS</span></span>

[<span data-ttu-id="b8a28-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b8a28-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b8a28-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8a28-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="b8a28-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8a28-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b8a28-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8a28-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


