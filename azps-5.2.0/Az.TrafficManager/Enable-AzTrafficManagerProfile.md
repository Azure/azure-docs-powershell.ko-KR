---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326192"
---
# <span data-ttu-id="01ed2-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="01ed2-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="01ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="01ed2-103">Traffic Manager 프로필을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="01ed2-104">구문</span><span class="sxs-lookup"><span data-stu-id="01ed2-104">SYNTAX</span></span>

### <span data-ttu-id="01ed2-105">필드</span><span class="sxs-lookup"><span data-stu-id="01ed2-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ed2-106">개체</span><span class="sxs-lookup"><span data-stu-id="01ed2-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ed2-107">설명</span><span class="sxs-lookup"><span data-stu-id="01ed2-107">DESCRIPTION</span></span>
<span data-ttu-id="01ed2-108">**Enable-AzTrafficManagerProfile** cmdlet을 사용하면 Azure Traffic Manager 프로필을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="01ed2-109">파이프라인을 사용하여 또는 매개 변수 값으로 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="01ed2-110">또는 Name 및 *ResourceGroupName* 매개 변수를 사용하여 프로필을 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="01ed2-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="01ed2-111">예제</span><span class="sxs-lookup"><span data-stu-id="01ed2-111">EXAMPLES</span></span>

### <span data-ttu-id="01ed2-112">예제 1: 이름으로 지정된 프로필 사용</span><span class="sxs-lookup"><span data-stu-id="01ed2-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="01ed2-113">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="01ed2-114">예제 2: 파이프라인을 사용하여 프로필 사용</span><span class="sxs-lookup"><span data-stu-id="01ed2-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="01ed2-115">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="01ed2-116">그런 다음 이 명령은 파이프라인 연산자를 사용하여 해당 프로필을 **Enable-AzTrafficManagerProfile** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="01ed2-117">이 cmdlet을 사용하면 프로필을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="01ed2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01ed2-118">PARAMETERS</span></span>

### <span data-ttu-id="01ed2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ed2-119">-DefaultProfile</span></span>
<span data-ttu-id="01ed2-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01ed2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="01ed2-121">-Name</span></span>
<span data-ttu-id="01ed2-122">이 cmdlet에서 사용할 수 있는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ed2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ed2-123">-ResourceGroupName</span></span>
<span data-ttu-id="01ed2-124">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="01ed2-125">이 cmdlet을 사용하면 이 매개 변수가 지정하는 그룹에서 Traffic Manager 프로필을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ed2-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="01ed2-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="01ed2-127">사용할 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="01ed2-128">**TrafficManagerProfile** 개체를 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01ed2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ed2-129">CommonParameters</span></span>
<span data-ttu-id="01ed2-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01ed2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ed2-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="01ed2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ed2-132">입력</span><span class="sxs-lookup"><span data-stu-id="01ed2-132">INPUTS</span></span>

### <span data-ttu-id="01ed2-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="01ed2-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="01ed2-134">출력</span><span class="sxs-lookup"><span data-stu-id="01ed2-134">OUTPUTS</span></span>

### <span data-ttu-id="01ed2-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01ed2-135">System.Boolean</span></span>

## <span data-ttu-id="01ed2-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01ed2-136">NOTES</span></span>

## <span data-ttu-id="01ed2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01ed2-137">RELATED LINKS</span></span>

[<span data-ttu-id="01ed2-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="01ed2-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="01ed2-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="01ed2-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="01ed2-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="01ed2-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="01ed2-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="01ed2-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="01ed2-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="01ed2-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


