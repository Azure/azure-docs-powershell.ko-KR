---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218449"
---
# <span data-ttu-id="8f2c5-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f2c5-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="8f2c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2c5-103">Traffic Manager에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="8f2c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f2c5-104">SYNTAX</span></span>

### <span data-ttu-id="8f2c5-105">필드인</span><span class="sxs-lookup"><span data-stu-id="8f2c5-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f2c5-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="8f2c5-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f2c5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8f2c5-107">DESCRIPTION</span></span>
<span data-ttu-id="8f2c5-108">**AzTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="8f2c5-109">이 cmdlet은 트래픽 관리자 서비스에 대 한 각 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="8f2c5-110">로컬 트래픽 관리자 프로필 개체에서 여러 끝점을 제거 하 고 한 번의 작업으로 변경 내용을 커밋하려면 Remove-AzTrafficManagerEndpointConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="8f2c5-111">파이프라인 연산자를 사용 하 여이 cmdlet에 **TrafficManagerEndpoint** 개체를 전달 하거나 *TrafficManagerEndpoint* 매개 변수를 사용 하 여 **TrafficManagerEndpoint** 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="8f2c5-112">또는 *name* 및 *type* 매개 변수를 사용 하 여 */profile* 및 *ResourceGroupName* 매개 변수와 함께 끝점 이름과 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="8f2c5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="8f2c5-113">EXAMPLES</span></span>

### <span data-ttu-id="8f2c5-114">예제 1: 프로필에서 끝점 제거</span><span class="sxs-lookup"><span data-stu-id="8f2c5-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="8f2c5-115">이 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 ContosoProfile 이라는 프로필에서 contoso 라는 Azure 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="8f2c5-116">변수</span><span class="sxs-lookup"><span data-stu-id="8f2c5-116">PARAMETERS</span></span>

### <span data-ttu-id="8f2c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2c5-117">-DefaultProfile</span></span>
<span data-ttu-id="8f2c5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f2c5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8f2c5-119">-Force</span></span>
<span data-ttu-id="8f2c5-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f2c5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8f2c5-121">-Name</span></span>
<span data-ttu-id="8f2c5-122">이 cmdlet이 제거 하는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8f2c5-123">-/Profile</span><span class="sxs-lookup"><span data-stu-id="8f2c5-123">-ProfileName</span></span>
<span data-ttu-id="8f2c5-124">이 cmdlet이 끝점을 제거 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="8f2c5-125">프로필을 얻으려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="8f2c5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2c5-126">-ResourceGroupName</span></span>
<span data-ttu-id="8f2c5-127">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8f2c5-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹의 Traffic Manager 프로필에서 Traffic Manager 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8f2c5-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f2c5-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="8f2c5-130">이 cmdlet이 제거 하는 트래픽 관리자 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="8f2c5-131">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="8f2c5-132">-Type</span><span class="sxs-lookup"><span data-stu-id="8f2c5-132">-Type</span></span>
<span data-ttu-id="8f2c5-133">이 cmdlet이 Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="8f2c5-134">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-134">Valid values are:</span></span> 

- <span data-ttu-id="8f2c5-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="8f2c5-135">AzureEndpoints</span></span>
- <span data-ttu-id="8f2c5-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="8f2c5-136">ExternalEndpoints</span></span>
- <span data-ttu-id="8f2c5-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="8f2c5-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="8f2c5-138">-확인</span><span class="sxs-lookup"><span data-stu-id="8f2c5-138">-Confirm</span></span>
<span data-ttu-id="8f2c5-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f2c5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2c5-140">-WhatIf</span></span>
<span data-ttu-id="8f2c5-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f2c5-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f2c5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2c5-143">CommonParameters</span></span>
<span data-ttu-id="8f2c5-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2c5-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f2c5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2c5-146">입력</span><span class="sxs-lookup"><span data-stu-id="8f2c5-146">INPUTS</span></span>

### <span data-ttu-id="8f2c5-147">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8f2c5-148">출력</span><span class="sxs-lookup"><span data-stu-id="8f2c5-148">OUTPUTS</span></span>

### <span data-ttu-id="8f2c5-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8f2c5-149">System.Boolean</span></span>

## <span data-ttu-id="8f2c5-150">상속자</span><span class="sxs-lookup"><span data-stu-id="8f2c5-150">NOTES</span></span>

## <span data-ttu-id="8f2c5-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f2c5-151">RELATED LINKS</span></span>

[<span data-ttu-id="8f2c5-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f2c5-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8f2c5-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f2c5-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8f2c5-154">새로운 AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f2c5-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8f2c5-155">제거-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="8f2c5-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="8f2c5-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f2c5-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


