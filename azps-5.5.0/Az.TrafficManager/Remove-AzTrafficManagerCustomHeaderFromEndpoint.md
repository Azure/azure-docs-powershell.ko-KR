---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198241"
---
# <span data-ttu-id="77116-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="77116-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="77116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77116-102">SYNOPSIS</span></span>
<span data-ttu-id="77116-103">로컬 Traffic Manager 엔드포인트 개체에서 사용자 지정 헤더 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="77116-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="77116-104">구문</span><span class="sxs-lookup"><span data-stu-id="77116-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77116-105">설명</span><span class="sxs-lookup"><span data-stu-id="77116-105">DESCRIPTION</span></span>
<span data-ttu-id="77116-106">**Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet은 로컬 Azure Traffic Manager 엔드포인트 개체에서 사용자 지정 헤더 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="77116-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="77116-107">New-AzTrafficManagerEndpoint cmdlet을 사용하여 엔드포인트를 Get-AzTrafficManagerEndpoint 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77116-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="77116-108">이 cmdlet은 로컬 엔드포인트 개체에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="77116-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="77116-109">Set-AzTrafficManagerEndpoint cmdlet을 사용하여 Traffic Manager에 대한 엔드포인트에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="77116-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="77116-110">예제</span><span class="sxs-lookup"><span data-stu-id="77116-110">EXAMPLES</span></span>

### <span data-ttu-id="77116-111">예제 1: 엔드포인트에서 사용자 지정 서브넷 정보 제거</span><span class="sxs-lookup"><span data-stu-id="77116-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="77116-112">첫 번째 명령은 ResourceGroup11이라는 리소스 그룹의 ContosoProfile 프로필에서 contoso라는 Azure 엔드포인트를 끈 다음, 해당 개체를 $TrafficManagerEndpoint 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="77116-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="77116-113">두 번째 명령은 사용자 지정 헤더 정보를 사용자 지정 헤더에 저장된 엔드포인트에서 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="77116-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="77116-114">마지막 명령은 Traffic Manager의 엔드포인트를 업데이트하여 트래픽 관리자의 로컬 값과 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="77116-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="77116-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77116-115">PARAMETERS</span></span>

### <span data-ttu-id="77116-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77116-116">-DefaultProfile</span></span>
<span data-ttu-id="77116-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77116-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77116-118">-Name</span><span class="sxs-lookup"><span data-stu-id="77116-118">-Name</span></span>
<span data-ttu-id="77116-119">제거할 사용자 지정 헤더 정보의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="77116-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="77116-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="77116-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="77116-121">로컬 **TrafficManagerEndpoint 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="77116-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="77116-122">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="77116-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="77116-123">**TrafficManagerEndpoint** 개체를 얻습니다. Get-AzTrafficManagerEndpoint 또는 New-AzTrafficManagerEndpoint 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="77116-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77116-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77116-124">-Confirm</span></span>
<span data-ttu-id="77116-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="77116-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77116-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77116-126">-WhatIf</span></span>
<span data-ttu-id="77116-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="77116-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77116-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77116-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77116-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77116-129">CommonParameters</span></span>
<span data-ttu-id="77116-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77116-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77116-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="77116-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77116-132">입력</span><span class="sxs-lookup"><span data-stu-id="77116-132">INPUTS</span></span>

### <span data-ttu-id="77116-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="77116-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="77116-134">출력</span><span class="sxs-lookup"><span data-stu-id="77116-134">OUTPUTS</span></span>

### <span data-ttu-id="77116-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="77116-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="77116-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77116-136">NOTES</span></span>

## <span data-ttu-id="77116-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77116-137">RELATED LINKS</span></span>

[<span data-ttu-id="77116-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="77116-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="77116-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="77116-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="77116-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="77116-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="77116-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="77116-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
