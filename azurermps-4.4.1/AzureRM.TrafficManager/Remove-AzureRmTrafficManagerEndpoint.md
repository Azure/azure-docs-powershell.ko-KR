---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 04053050720f2639eeeb698dcfbffb3e156fe2c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529969"
---
# <span data-ttu-id="937a2-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="937a2-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="937a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="937a2-102">SYNOPSIS</span></span>
<span data-ttu-id="937a2-103">Traffic Manager에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="937a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="937a2-104">SYNTAX</span></span>

### <span data-ttu-id="937a2-105">필드인</span><span class="sxs-lookup"><span data-stu-id="937a2-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="937a2-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="937a2-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="937a2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="937a2-107">DESCRIPTION</span></span>
<span data-ttu-id="937a2-108">**AzureRmTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="937a2-109">이 cmdlet은 트래픽 관리자 서비스에 대 한 각 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="937a2-110">로컬 트래픽 관리자 프로필 개체에서 여러 끝점을 제거 하 고 한 번의 작업으로 변경 내용을 커밋하려면 Remove-AzureRmTrafficManagerEndpointConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="937a2-111">파이프라인 연산자를 사용 하 여이 cmdlet에 **TrafficManagerEndpoint** 개체를 전달 하거나 *TrafficManagerEndpoint* 매개 변수를 사용 하 여 **TrafficManagerEndpoint** 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="937a2-112">또는 *name* 및 *type* 매개 변수를 사용 하 여 */profile* 및 *ResourceGroupName* 매개 변수와 함께 끝점 이름과 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="937a2-113">예제의</span><span class="sxs-lookup"><span data-stu-id="937a2-113">EXAMPLES</span></span>

### <span data-ttu-id="937a2-114">예제 1: 프로필에서 끝점 제거</span><span class="sxs-lookup"><span data-stu-id="937a2-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="937a2-115">이 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 ContosoProfile 이라는 프로필에서 contoso 라는 Azure 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="937a2-116">변수</span><span class="sxs-lookup"><span data-stu-id="937a2-116">PARAMETERS</span></span>

### <span data-ttu-id="937a2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="937a2-117">-Force</span></span>
<span data-ttu-id="937a2-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="937a2-119">-이름</span><span class="sxs-lookup"><span data-stu-id="937a2-119">-Name</span></span>
<span data-ttu-id="937a2-120">이 cmdlet이 제거 하는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-120">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="937a2-121">-/Profile</span><span class="sxs-lookup"><span data-stu-id="937a2-121">-ProfileName</span></span>
<span data-ttu-id="937a2-122">이 cmdlet이 끝점을 제거 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-122">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="937a2-123">프로필을 얻으려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-123">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="937a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="937a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="937a2-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-125">Specifies the name of a resource group.</span></span>
<span data-ttu-id="937a2-126">이 cmdlet은이 매개 변수에서 지정 하는 그룹의 Traffic Manager 프로필에서 Traffic Manager 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-126">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="937a2-127">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="937a2-127">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="937a2-128">이 cmdlet이 제거 하는 트래픽 관리자 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-128">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="937a2-129">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzureRmTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="937a2-130">-Type</span><span class="sxs-lookup"><span data-stu-id="937a2-130">-Type</span></span>
<span data-ttu-id="937a2-131">이 cmdlet이 Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-131">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="937a2-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-132">Valid values are:</span></span> 

- <span data-ttu-id="937a2-133">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="937a2-133">AzureEndpoints</span></span>
- <span data-ttu-id="937a2-134">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="937a2-134">ExternalEndpoints</span></span>
- <span data-ttu-id="937a2-135">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="937a2-135">NestedEndpoints</span></span>

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

### <span data-ttu-id="937a2-136">-확인</span><span class="sxs-lookup"><span data-stu-id="937a2-136">-Confirm</span></span>
<span data-ttu-id="937a2-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="937a2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="937a2-138">-WhatIf</span></span>
<span data-ttu-id="937a2-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="937a2-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="937a2-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937a2-141">-DefaultProfile</span></span>
<span data-ttu-id="937a2-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="937a2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937a2-143">CommonParameters</span></span>
<span data-ttu-id="937a2-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937a2-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="937a2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937a2-146">입력</span><span class="sxs-lookup"><span data-stu-id="937a2-146">INPUTS</span></span>

### <span data-ttu-id="937a2-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="937a2-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="937a2-148">' TrafficManagerEndpoint ' 매개 변수는 파이프라인에서 ' TrafficManagerEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="937a2-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="937a2-149">출력</span><span class="sxs-lookup"><span data-stu-id="937a2-149">OUTPUTS</span></span>

### <span data-ttu-id="937a2-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="937a2-150">System.Boolean</span></span>

## <span data-ttu-id="937a2-151">상속자</span><span class="sxs-lookup"><span data-stu-id="937a2-151">NOTES</span></span>

## <span data-ttu-id="937a2-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="937a2-152">RELATED LINKS</span></span>

[<span data-ttu-id="937a2-153">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="937a2-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="937a2-154">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="937a2-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="937a2-155">새로운 AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="937a2-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="937a2-156">제거-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="937a2-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="937a2-157">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="937a2-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


