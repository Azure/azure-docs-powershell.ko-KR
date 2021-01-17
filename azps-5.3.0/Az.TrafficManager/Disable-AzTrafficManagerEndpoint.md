---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382922"
---
# <span data-ttu-id="0d65f-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d65f-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="0d65f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d65f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d65f-103">Traffic Manager 프로필에서 엔드포인트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="0d65f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d65f-104">SYNTAX</span></span>

### <span data-ttu-id="0d65f-105">필드</span><span class="sxs-lookup"><span data-stu-id="0d65f-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d65f-106">개체</span><span class="sxs-lookup"><span data-stu-id="0d65f-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d65f-107">설명</span><span class="sxs-lookup"><span data-stu-id="0d65f-107">DESCRIPTION</span></span>
<span data-ttu-id="0d65f-108">**Disable-AzTrafficManagerEndpoint** cmdlet은 Azure Traffic Manager 프로필에서 엔드포인트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="0d65f-109">파이프라인 연산자를 사용하여 **TrafficManagerEndpoint** 개체를 이 cmdlet에 전달하거나 **TrafficManagerEndpoint** 매개 변수를 사용하여 *TrafficManagerEndpoint* 개체를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="0d65f-110">또는 *ProfileName* 및 *ResourceGroupName*  매개 변수와 함께 이름 및 *형식* 매개 변수를 사용하여 엔드포인트 이름 및 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="0d65f-111">예제</span><span class="sxs-lookup"><span data-stu-id="0d65f-111">EXAMPLES</span></span>

### <span data-ttu-id="0d65f-112">예제 1: 이름으로 엔드포인트 사용 안</span><span class="sxs-lookup"><span data-stu-id="0d65f-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="0d65f-113">이 명령은 리소스 그룹 ResourceGroup11의 ContosoProfile 프로필에서 contoso라는 외부 엔드포인트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="0d65f-114">이 명령은 확인을 요청하는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="0d65f-115">예제 2: 파이프라인을 사용하여 엔드포인트 비활성화</span><span class="sxs-lookup"><span data-stu-id="0d65f-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="0d65f-116">이 명령은 ResourceGroup11의 ContosoProfile 프로필에서 Contoso라는 외부 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="0d65f-117">그런 다음 이 명령은 파이프라인 연산자를 사용하여 해당 엔드포인트를 **Disable-AzTrafficManagerEndpoint** cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0d65f-118">이 cmdlet은 엔드포인트를 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="0d65f-119">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="0d65f-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0d65f-120">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0d65f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d65f-121">PARAMETERS</span></span>

### <span data-ttu-id="0d65f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d65f-122">-DefaultProfile</span></span>
<span data-ttu-id="0d65f-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d65f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0d65f-124">-Force</span></span>
<span data-ttu-id="0d65f-125">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0d65f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0d65f-126">-Name</span></span>
<span data-ttu-id="0d65f-127">이 cmdlet에서 사용하지 않도록 설정하는 Traffic Manager 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="0d65f-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0d65f-128">-ProfileName</span></span>
<span data-ttu-id="0d65f-129">이 cmdlet이 엔드포인트를 사용하지 않도록 설정하는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="0d65f-130">프로필을 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="0d65f-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="0d65f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d65f-131">-ResourceGroupName</span></span>
<span data-ttu-id="0d65f-132">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0d65f-133">이 cmdlet은 이 매개 변수가 지정하는 그룹에서 Traffic Manager 엔드포인트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0d65f-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d65f-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="0d65f-135">이 cmdlet에서 사용하지 않도록 설정하는 Traffic Manager 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="0d65f-136">**TrafficManagerEndpoint** 개체를 얻습니다. Get-AzTrafficManagerEndpoint cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="0d65f-137">-Type</span><span class="sxs-lookup"><span data-stu-id="0d65f-137">-Type</span></span>
<span data-ttu-id="0d65f-138">이 cmdlet이 Traffic Manager 프로필에 추가하는 엔드포인트의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="0d65f-139">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="0d65f-139">Valid values are:</span></span> 

- <span data-ttu-id="0d65f-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="0d65f-140">AzureEndpoints</span></span>
- <span data-ttu-id="0d65f-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="0d65f-141">ExternalEndpoints</span></span>
- <span data-ttu-id="0d65f-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="0d65f-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="0d65f-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d65f-143">-Confirm</span></span>
<span data-ttu-id="0d65f-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d65f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d65f-145">-WhatIf</span></span>
<span data-ttu-id="0d65f-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0d65f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d65f-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d65f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d65f-148">CommonParameters</span></span>
<span data-ttu-id="0d65f-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d65f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d65f-150">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0d65f-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d65f-151">입력</span><span class="sxs-lookup"><span data-stu-id="0d65f-151">INPUTS</span></span>

### <span data-ttu-id="0d65f-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d65f-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0d65f-153">출력</span><span class="sxs-lookup"><span data-stu-id="0d65f-153">OUTPUTS</span></span>

### <span data-ttu-id="0d65f-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d65f-154">System.Boolean</span></span>

## <span data-ttu-id="0d65f-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d65f-155">NOTES</span></span>

## <span data-ttu-id="0d65f-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d65f-156">RELATED LINKS</span></span>

[<span data-ttu-id="0d65f-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d65f-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0d65f-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d65f-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0d65f-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d65f-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="0d65f-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d65f-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0d65f-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d65f-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="0d65f-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d65f-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0d65f-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d65f-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


