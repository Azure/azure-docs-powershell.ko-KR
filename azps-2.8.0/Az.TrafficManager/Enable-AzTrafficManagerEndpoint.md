---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 99915859798eba5acb78fc62a5a5c56cff2ce791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872218"
---
# <span data-ttu-id="abf5e-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf5e-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="abf5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf5e-102">SYNOPSIS</span></span>
<span data-ttu-id="abf5e-103">Traffic Manager 프로필에서 끝점을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="abf5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="abf5e-104">SYNTAX</span></span>

### <span data-ttu-id="abf5e-105">필드인</span><span class="sxs-lookup"><span data-stu-id="abf5e-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abf5e-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="abf5e-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abf5e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="abf5e-107">DESCRIPTION</span></span>
<span data-ttu-id="abf5e-108">AzTrafficManagerEndpoint cmdlet을 **사용** 하면 Azure Traffic Manager 프로필에서 끝점을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="abf5e-109">파이프라인 연산자를 사용 하 여이 cmdlet에 **TrafficManagerEndpoint** 개체를 전달 하거나 *TrafficManagerEndpoint* 매개 변수를 사용 하 여 **TrafficManagerEndpoint** 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="abf5e-110">또는 *name* 및 *type* 매개 변수를 사용 하 여 */profile* 및 *ResourceGroupName* 매개 변수와 함께 끝점 이름과 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="abf5e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="abf5e-111">EXAMPLES</span></span>

### <span data-ttu-id="abf5e-112">예제 1: 프로필에서 끝점 사용</span><span class="sxs-lookup"><span data-stu-id="abf5e-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="abf5e-113">이 명령을 사용 하 여 리소스 그룹 ResourceGroup11의 ContosoProfile 이라는 프로필에 contoso 라는 외부 끝점을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="abf5e-114">예제 2: 파이프라인을 사용 하 여 끝점 활성화</span><span class="sxs-lookup"><span data-stu-id="abf5e-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="abf5e-115">이 명령은 ResourceGroup11의 ContosoProfile 이라는 프로필에서 Contoso 라는 외부 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="abf5e-116">그런 다음 파이프라인 연산자를 사용 하 여 해당 끝점을 **Enable-AzTrafficManagerEndpoint** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="abf5e-117">해당 cmdlet은 해당 끝점을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="abf5e-118">변수</span><span class="sxs-lookup"><span data-stu-id="abf5e-118">PARAMETERS</span></span>

### <span data-ttu-id="abf5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf5e-119">-DefaultProfile</span></span>
<span data-ttu-id="abf5e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf5e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="abf5e-121">-Name</span></span>
<span data-ttu-id="abf5e-122">이 cmdlet이 사용할 수 있는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="abf5e-123">-/Profile</span><span class="sxs-lookup"><span data-stu-id="abf5e-123">-ProfileName</span></span>
<span data-ttu-id="abf5e-124">이 cmdlet이 끝점을 사용할 수 있도록 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="abf5e-125">프로필을 얻으려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="abf5e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf5e-126">-ResourceGroupName</span></span>
<span data-ttu-id="abf5e-127">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="abf5e-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 끝점을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="abf5e-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf5e-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="abf5e-130">이 cmdlet이 사용할 수 있는 트래픽 관리자 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="abf5e-131">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="abf5e-132">-Type</span><span class="sxs-lookup"><span data-stu-id="abf5e-132">-Type</span></span>
<span data-ttu-id="abf5e-133">이 cmdlet이 Traffic Manager 프로필에서 사용 하지 않도록 설정 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="abf5e-134">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-134">Valid values are:</span></span> 

- <span data-ttu-id="abf5e-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="abf5e-135">AzureEndpoints</span></span>
- <span data-ttu-id="abf5e-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="abf5e-136">ExternalEndpoints</span></span>
- <span data-ttu-id="abf5e-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="abf5e-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="abf5e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf5e-138">CommonParameters</span></span>
<span data-ttu-id="abf5e-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf5e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf5e-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf5e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf5e-141">입력</span><span class="sxs-lookup"><span data-stu-id="abf5e-141">INPUTS</span></span>

### <span data-ttu-id="abf5e-142">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="abf5e-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="abf5e-143">출력</span><span class="sxs-lookup"><span data-stu-id="abf5e-143">OUTPUTS</span></span>

### <span data-ttu-id="abf5e-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="abf5e-144">System.Boolean</span></span>

## <span data-ttu-id="abf5e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="abf5e-145">NOTES</span></span>

## <span data-ttu-id="abf5e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abf5e-146">RELATED LINKS</span></span>

[<span data-ttu-id="abf5e-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf5e-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="abf5e-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf5e-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="abf5e-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="abf5e-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="abf5e-150">새로운 AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf5e-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="abf5e-151">새로운 AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="abf5e-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="abf5e-152">제거-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf5e-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="abf5e-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="abf5e-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


