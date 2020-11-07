---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 196cdd5f41a33fe0e4185c4f30a35ce9444139de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698409"
---
# <span data-ttu-id="bf9ee-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf9ee-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="bf9ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9ee-103">Traffic Manager 프로필에서 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="bf9ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf9ee-104">SYNTAX</span></span>

### <span data-ttu-id="bf9ee-105">필드인</span><span class="sxs-lookup"><span data-stu-id="bf9ee-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf9ee-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="bf9ee-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf9ee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bf9ee-107">DESCRIPTION</span></span>
<span data-ttu-id="bf9ee-108">**AzTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager 프로필에서 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="bf9ee-109">파이프라인 연산자를 사용 하 여 **TrafficManagerEndpoint** 개체를이 cmdlet에 전달 하거나 *TrafficManagerEndpoint* 매개 변수를 사용 하 여 **TrafficManagerEndpoint** 개체를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="bf9ee-110">또는 *name* 및 *type* 매개 변수를 사용 하 여 */profile* 및 *ResourceGroupName* 매개 변수와 함께 끝점 이름과 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="bf9ee-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bf9ee-111">EXAMPLES</span></span>

### <span data-ttu-id="bf9ee-112">예제 1: 이름으로 끝점 비활성화</span><span class="sxs-lookup"><span data-stu-id="bf9ee-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="bf9ee-113">이 명령은 리소스 그룹 ResouceGroup11의 ContosoProfile 이라는 프로필에서 contoso 라는 외부 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="bf9ee-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="bf9ee-115">예제 2: 파이프라인을 사용 하 여 끝점 비활성화</span><span class="sxs-lookup"><span data-stu-id="bf9ee-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="bf9ee-116">이 명령은 ResourceGroup11의 ContosoProfile 이라는 프로필에서 Contoso 라는 외부 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="bf9ee-117">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 끝점을 **AzTrafficManagerEndpoint** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf9ee-118">해당 cmdlet은 해당 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="bf9ee-119">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="bf9ee-120">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bf9ee-121">변수</span><span class="sxs-lookup"><span data-stu-id="bf9ee-121">PARAMETERS</span></span>

### <span data-ttu-id="bf9ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9ee-122">-DefaultProfile</span></span>
<span data-ttu-id="bf9ee-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf9ee-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bf9ee-124">-Force</span></span>
<span data-ttu-id="bf9ee-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf9ee-126">-이름</span><span class="sxs-lookup"><span data-stu-id="bf9ee-126">-Name</span></span>
<span data-ttu-id="bf9ee-127">이 cmdlet이 사용 하지 않도록 설정 하는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="bf9ee-128">-/Profile</span><span class="sxs-lookup"><span data-stu-id="bf9ee-128">-ProfileName</span></span>
<span data-ttu-id="bf9ee-129">이 cmdlet이 끝점을 사용 하지 않도록 설정 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="bf9ee-130">프로필을 얻으려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="bf9ee-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9ee-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf9ee-132">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bf9ee-133">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf9ee-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf9ee-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="bf9ee-135">이 cmdlet이 사용 하지 않도록 설정 하는 트래픽 관리자 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="bf9ee-136">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="bf9ee-137">-Type</span><span class="sxs-lookup"><span data-stu-id="bf9ee-137">-Type</span></span>
<span data-ttu-id="bf9ee-138">이 cmdlet이 Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="bf9ee-139">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-139">Valid values are:</span></span> 

- <span data-ttu-id="bf9ee-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="bf9ee-140">AzureEndpoints</span></span>
- <span data-ttu-id="bf9ee-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="bf9ee-141">ExternalEndpoints</span></span>
- <span data-ttu-id="bf9ee-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="bf9ee-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="bf9ee-143">-확인</span><span class="sxs-lookup"><span data-stu-id="bf9ee-143">-Confirm</span></span>
<span data-ttu-id="bf9ee-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf9ee-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf9ee-145">-WhatIf</span></span>
<span data-ttu-id="bf9ee-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf9ee-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf9ee-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9ee-148">CommonParameters</span></span>
<span data-ttu-id="bf9ee-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9ee-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf9ee-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9ee-151">입력</span><span class="sxs-lookup"><span data-stu-id="bf9ee-151">INPUTS</span></span>

### <span data-ttu-id="bf9ee-152">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="bf9ee-153">출력</span><span class="sxs-lookup"><span data-stu-id="bf9ee-153">OUTPUTS</span></span>

### <span data-ttu-id="bf9ee-154">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bf9ee-154">System.Boolean</span></span>

## <span data-ttu-id="bf9ee-155">상속자</span><span class="sxs-lookup"><span data-stu-id="bf9ee-155">NOTES</span></span>

## <span data-ttu-id="bf9ee-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf9ee-156">RELATED LINKS</span></span>

[<span data-ttu-id="bf9ee-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf9ee-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bf9ee-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf9ee-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bf9ee-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf9ee-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="bf9ee-160">새로운 AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf9ee-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bf9ee-161">새로운 AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf9ee-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="bf9ee-162">제거-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf9ee-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="bf9ee-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bf9ee-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


