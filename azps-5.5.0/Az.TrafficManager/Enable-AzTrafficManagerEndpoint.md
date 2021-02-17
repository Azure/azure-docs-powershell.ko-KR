---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198265"
---
# <span data-ttu-id="bd7d5-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd7d5-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="bd7d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7d5-103">Traffic Manager 프로필에서 엔드포인트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="bd7d5-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd7d5-104">SYNTAX</span></span>

### <span data-ttu-id="bd7d5-105">필드</span><span class="sxs-lookup"><span data-stu-id="bd7d5-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd7d5-106">개체</span><span class="sxs-lookup"><span data-stu-id="bd7d5-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd7d5-107">설명</span><span class="sxs-lookup"><span data-stu-id="bd7d5-107">DESCRIPTION</span></span>
<span data-ttu-id="bd7d5-108">**Enable-AzTrafficManagerEndpoint** cmdlet을 사용하면 Azure Traffic Manager 프로필에서 엔드포인트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="bd7d5-109">파이프라인 연산자를 사용하여 **TrafficManagerEndpoint** 개체를 이 cmdlet에 전달하거나 **TrafficManagerEndpoint** 매개 변수를 사용하여 *TrafficManagerEndpoint* 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="bd7d5-110">또는 *ProfileName* 및 *ResourceGroupName*  매개 변수와 함께 이름 및 *형식* 매개 변수를 사용하여 엔드포인트 이름 및 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="bd7d5-111">예제</span><span class="sxs-lookup"><span data-stu-id="bd7d5-111">EXAMPLES</span></span>

### <span data-ttu-id="bd7d5-112">예제 1: 프로필에서 엔드포인트 사용</span><span class="sxs-lookup"><span data-stu-id="bd7d5-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="bd7d5-113">이 명령은 리소스 그룹 ResourceGroup11의 ContosoProfile 프로필에서 contoso라는 외부 엔드포인트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="bd7d5-114">예제 2: 파이프라인을 사용하여 엔드포인트 사용</span><span class="sxs-lookup"><span data-stu-id="bd7d5-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="bd7d5-115">이 명령은 ResourceGroup11의 ContosoProfile 프로필에서 Contoso라는 외부 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="bd7d5-116">그런 다음 이 명령은 파이프라인 연산자를 사용하여 해당 엔드포인트를 **Enable-AzTrafficManagerEndpoint** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bd7d5-117">이 cmdlet은 엔드포인트를 가능하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="bd7d5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd7d5-118">PARAMETERS</span></span>

### <span data-ttu-id="bd7d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7d5-119">-DefaultProfile</span></span>
<span data-ttu-id="bd7d5-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd7d5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bd7d5-121">-Name</span></span>
<span data-ttu-id="bd7d5-122">이 cmdlet에서 사용 가능하게 하는 Traffic Manager 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="bd7d5-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bd7d5-123">-ProfileName</span></span>
<span data-ttu-id="bd7d5-124">이 cmdlet에서 엔드포인트를 사용할 수 있는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="bd7d5-125">프로필을 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="bd7d5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7d5-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd7d5-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bd7d5-128">이 cmdlet을 사용하면 이 매개 변수가 지정하는 그룹의 Traffic Manager 엔드포인트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bd7d5-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd7d5-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="bd7d5-130">이 cmdlet에서 사용 가능하게 하는 Traffic Manager 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="bd7d5-131">**TrafficManagerEndpoint** 개체를 얻습니다. Get-AzTrafficManagerEndpoint cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d5-132">-Type</span><span class="sxs-lookup"><span data-stu-id="bd7d5-132">-Type</span></span>
<span data-ttu-id="bd7d5-133">Traffic Manager 프로필에서 이 cmdlet을 사용하지 않도록 설정하는 엔드포인트의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="bd7d5-134">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="bd7d5-134">Valid values are:</span></span> 

- <span data-ttu-id="bd7d5-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="bd7d5-135">AzureEndpoints</span></span>
- <span data-ttu-id="bd7d5-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="bd7d5-136">ExternalEndpoints</span></span>
- <span data-ttu-id="bd7d5-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="bd7d5-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7d5-138">CommonParameters</span></span>
<span data-ttu-id="bd7d5-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7d5-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bd7d5-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7d5-141">입력</span><span class="sxs-lookup"><span data-stu-id="bd7d5-141">INPUTS</span></span>

### <span data-ttu-id="bd7d5-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd7d5-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="bd7d5-143">출력</span><span class="sxs-lookup"><span data-stu-id="bd7d5-143">OUTPUTS</span></span>

### <span data-ttu-id="bd7d5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bd7d5-144">System.Boolean</span></span>

## <span data-ttu-id="bd7d5-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd7d5-145">NOTES</span></span>

## <span data-ttu-id="bd7d5-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd7d5-146">RELATED LINKS</span></span>

[<span data-ttu-id="bd7d5-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd7d5-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bd7d5-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd7d5-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bd7d5-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bd7d5-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="bd7d5-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd7d5-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bd7d5-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bd7d5-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="bd7d5-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd7d5-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bd7d5-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bd7d5-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


