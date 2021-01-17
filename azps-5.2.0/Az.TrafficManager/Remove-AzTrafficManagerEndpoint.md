---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330398"
---
# <span data-ttu-id="2f649-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f649-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="2f649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f649-102">SYNOPSIS</span></span>
<span data-ttu-id="2f649-103">Traffic Manager에서 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="2f649-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f649-104">SYNTAX</span></span>

### <span data-ttu-id="2f649-105">필드</span><span class="sxs-lookup"><span data-stu-id="2f649-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f649-106">개체</span><span class="sxs-lookup"><span data-stu-id="2f649-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f649-107">설명</span><span class="sxs-lookup"><span data-stu-id="2f649-107">DESCRIPTION</span></span>
<span data-ttu-id="2f649-108">**Remove-AzTrafficManagerEndpoint** cmdlet은 Azure Traffic Manager에서 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="2f649-109">이 cmdlet은 Traffic Manager 서비스에 대한 각 변경을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="2f649-110">로컬 Traffic Manager 프로필 개체에서 여러 엔드포인트를 제거하고 단일 작업에서 변경 내용을 커밋하려면 Remove-AzTrafficManagerEndpointConfig cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="2f649-111">파이프라인 연산자를 사용하여 **TrafficManagerEndpoint** 개체를 이 cmdlet에 전달하거나 **TrafficManagerEndpoint** 매개 변수를 사용하여 *TrafficManagerEndpoint* 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="2f649-112">또는 *ProfileName* 및 *ResourceGroupName*  매개 변수와 함께 이름 및 *형식* 매개 변수를 사용하여 엔드포인트 이름 및 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="2f649-113">예제</span><span class="sxs-lookup"><span data-stu-id="2f649-113">EXAMPLES</span></span>

### <span data-ttu-id="2f649-114">예제 1: 프로필에서 엔드포인트 제거</span><span class="sxs-lookup"><span data-stu-id="2f649-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="2f649-115">이 명령은 ResourceGroup11이라는 리소스 그룹의 ContosoProfile 프로필에서 contoso라는 Azure 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2f649-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f649-116">PARAMETERS</span></span>

### <span data-ttu-id="2f649-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f649-117">-DefaultProfile</span></span>
<span data-ttu-id="2f649-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f649-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2f649-119">-Force</span></span>
<span data-ttu-id="2f649-120">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f649-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2f649-121">-Name</span></span>
<span data-ttu-id="2f649-122">이 cmdlet에서 제거하는 Traffic Manager 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f649-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2f649-123">-ProfileName</span></span>
<span data-ttu-id="2f649-124">이 cmdlet이 엔드포인트를 제거하는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="2f649-125">프로필을 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="2f649-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="2f649-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f649-126">-ResourceGroupName</span></span>
<span data-ttu-id="2f649-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2f649-128">이 cmdlet은 이 매개 변수가 지정하는 그룹의 Traffic Manager 프로필에서 Traffic Manager 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f649-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f649-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="2f649-130">이 cmdlet이 제거하는 Traffic Manager 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="2f649-131">**TrafficManagerEndpoint** 개체를 얻습니다. Get-AzTrafficManagerEndpoint cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="2f649-132">-Type</span><span class="sxs-lookup"><span data-stu-id="2f649-132">-Type</span></span>
<span data-ttu-id="2f649-133">이 cmdlet이 Traffic Manager 프로필에 추가하는 엔드포인트의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="2f649-134">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="2f649-134">Valid values are:</span></span> 

- <span data-ttu-id="2f649-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="2f649-135">AzureEndpoints</span></span>
- <span data-ttu-id="2f649-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="2f649-136">ExternalEndpoints</span></span>
- <span data-ttu-id="2f649-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="2f649-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="2f649-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f649-138">-Confirm</span></span>
<span data-ttu-id="2f649-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f649-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f649-140">-WhatIf</span></span>
<span data-ttu-id="2f649-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2f649-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f649-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f649-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f649-143">CommonParameters</span></span>
<span data-ttu-id="2f649-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f649-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f649-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2f649-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f649-146">입력</span><span class="sxs-lookup"><span data-stu-id="2f649-146">INPUTS</span></span>

### <span data-ttu-id="2f649-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f649-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2f649-148">출력</span><span class="sxs-lookup"><span data-stu-id="2f649-148">OUTPUTS</span></span>

### <span data-ttu-id="2f649-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f649-149">System.Boolean</span></span>

## <span data-ttu-id="2f649-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f649-150">NOTES</span></span>

## <span data-ttu-id="2f649-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f649-151">RELATED LINKS</span></span>

[<span data-ttu-id="2f649-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f649-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2f649-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2f649-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="2f649-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f649-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2f649-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2f649-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2f649-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2f649-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


