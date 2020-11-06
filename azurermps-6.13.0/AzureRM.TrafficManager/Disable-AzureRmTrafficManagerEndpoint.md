---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: af05a91fe2281d457cff649bf0de6d986f7f413a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530029"
---
# <span data-ttu-id="7e594-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e594-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="7e594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e594-102">SYNOPSIS</span></span>
<span data-ttu-id="7e594-103">Traffic Manager 프로필에서 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e594-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e594-104">SYNTAX</span></span>

### <span data-ttu-id="7e594-105">필드인</span><span class="sxs-lookup"><span data-stu-id="7e594-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e594-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="7e594-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e594-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7e594-107">DESCRIPTION</span></span>
<span data-ttu-id="7e594-108">**AzureRmTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager 프로필에서 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="7e594-109">파이프라인 연산자를 사용 하 여 **TrafficManagerEndpoint** 개체를이 cmdlet에 전달 하거나 *TrafficManagerEndpoint* 매개 변수를 사용 하 여 **TrafficManagerEndpoint** 개체를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="7e594-110">또는 *name* 및 *type* 매개 변수를 사용 하 여 */profile* 및 *ResourceGroupName* 매개 변수와 함께 끝점 이름과 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="7e594-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7e594-111">EXAMPLES</span></span>

### <span data-ttu-id="7e594-112">예제 1: 이름으로 끝점 비활성화</span><span class="sxs-lookup"><span data-stu-id="7e594-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="7e594-113">이 명령은 리소스 그룹 ResouceGroup11의 ContosoProfile 이라는 프로필에서 contoso 라는 외부 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="7e594-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7e594-115">예제 2: 파이프라인을 사용 하 여 끝점 비활성화</span><span class="sxs-lookup"><span data-stu-id="7e594-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="7e594-116">이 명령은 ResourceGroup11의 ContosoProfile 이라는 프로필에서 Contoso 라는 외부 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7e594-117">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 끝점을 **AzureRmTrafficManagerEndpoint** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e594-118">해당 cmdlet은 해당 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="7e594-119">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7e594-120">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7e594-121">변수</span><span class="sxs-lookup"><span data-stu-id="7e594-121">PARAMETERS</span></span>

### <span data-ttu-id="7e594-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e594-122">-DefaultProfile</span></span>
<span data-ttu-id="7e594-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e594-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7e594-124">-Force</span></span>
<span data-ttu-id="7e594-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e594-126">-이름</span><span class="sxs-lookup"><span data-stu-id="7e594-126">-Name</span></span>
<span data-ttu-id="7e594-127">이 cmdlet이 사용 하지 않도록 설정 하는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="7e594-128">-/Profile</span><span class="sxs-lookup"><span data-stu-id="7e594-128">-ProfileName</span></span>
<span data-ttu-id="7e594-129">이 cmdlet이 끝점을 사용 하지 않도록 설정 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="7e594-130">프로필을 얻으려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-130">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="7e594-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e594-131">-ResourceGroupName</span></span>
<span data-ttu-id="7e594-132">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7e594-133">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 끝점을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7e594-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e594-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="7e594-135">이 cmdlet이 사용 하지 않도록 설정 하는 트래픽 관리자 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="7e594-136">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzureRmTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="7e594-137">-Type</span><span class="sxs-lookup"><span data-stu-id="7e594-137">-Type</span></span>
<span data-ttu-id="7e594-138">이 cmdlet이 Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="7e594-139">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-139">Valid values are:</span></span> 

- <span data-ttu-id="7e594-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="7e594-140">AzureEndpoints</span></span>
- <span data-ttu-id="7e594-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="7e594-141">ExternalEndpoints</span></span>
- <span data-ttu-id="7e594-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="7e594-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="7e594-143">-확인</span><span class="sxs-lookup"><span data-stu-id="7e594-143">-Confirm</span></span>
<span data-ttu-id="7e594-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e594-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e594-145">-WhatIf</span></span>
<span data-ttu-id="7e594-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e594-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e594-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e594-148">CommonParameters</span></span>
<span data-ttu-id="7e594-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e594-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e594-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e594-151">입력</span><span class="sxs-lookup"><span data-stu-id="7e594-151">INPUTS</span></span>

### <span data-ttu-id="7e594-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e594-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="7e594-153">' TrafficManagerEndpoint ' 매개 변수는 파이프라인에서 ' TrafficManagerEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e594-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="7e594-154">출력</span><span class="sxs-lookup"><span data-stu-id="7e594-154">OUTPUTS</span></span>

### <span data-ttu-id="7e594-155">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7e594-155">System.Boolean</span></span>

## <span data-ttu-id="7e594-156">상속자</span><span class="sxs-lookup"><span data-stu-id="7e594-156">NOTES</span></span>

## <span data-ttu-id="7e594-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e594-157">RELATED LINKS</span></span>

[<span data-ttu-id="7e594-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e594-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7e594-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e594-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7e594-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e594-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7e594-161">새로운 AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e594-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7e594-162">새로운 AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e594-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7e594-163">제거-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e594-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7e594-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e594-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


