---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f0d179c82292ffb9300791337f40436c4d4c5f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987289"
---
# <span data-ttu-id="89fe2-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="89fe2-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="89fe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="89fe2-103">로컬 Traffic Manager 엔드포인트 개체에서 사용자 지정 헤더 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="89fe2-104">구문</span><span class="sxs-lookup"><span data-stu-id="89fe2-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89fe2-105">설명</span><span class="sxs-lookup"><span data-stu-id="89fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="89fe2-106">**Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet은 로컬 Azure Traffic Manager 엔드포인트 개체에서 사용자 지정 헤더 정보를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="89fe2-107">New-AzTrafficManagerEndpoint cmdlet을 사용하여 엔드포인트를 Get-AzTrafficManagerEndpoint 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="89fe2-108">이 cmdlet은 로컬 엔드포인트 개체에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="89fe2-109">cmdlet을 사용하여 Traffic Manager의 엔드포인트에 Set-AzTrafficManagerEndpoint 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="89fe2-110">예제</span><span class="sxs-lookup"><span data-stu-id="89fe2-110">EXAMPLES</span></span>

### <span data-ttu-id="89fe2-111">예제 1: 엔드포인트에서 사용자 지정 서브넷 정보 제거</span><span class="sxs-lookup"><span data-stu-id="89fe2-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="89fe2-112">첫 번째 명령은 ResourceGroup11이라는 리소스 그룹의 ContosoProfile이라는 프로필에서 contoso라는 Azure 엔드포인트를 한 다음, 해당 개체를 $TrafficManagerEndpoint 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="89fe2-113">두 번째 명령은 에 저장된 엔드포인트에서 사용자 지정 헤더 정보를 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="89fe2-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="89fe2-114">마지막 명령은 Traffic Manager의 엔드포인트를 업데이트하여 로컬 값과 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="89fe2-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="89fe2-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="89fe2-115">PARAMETERS</span></span>

### <span data-ttu-id="89fe2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fe2-116">-DefaultProfile</span></span>
<span data-ttu-id="89fe2-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89fe2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="89fe2-118">-Name</span></span>
<span data-ttu-id="89fe2-119">제거할 사용자 지정 헤더 정보의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="89fe2-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="89fe2-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="89fe2-121">로컬 **TrafficManagerEndpoint 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="89fe2-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="89fe2-122">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="89fe2-123">**TrafficManagerEndpoint** 개체를 얻은 경우 Get-AzTrafficManagerEndpoint cmdlet을 New-AzTrafficManagerEndpoint 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="89fe2-124">-확인</span><span class="sxs-lookup"><span data-stu-id="89fe2-124">-Confirm</span></span>
<span data-ttu-id="89fe2-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89fe2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89fe2-126">-WhatIf</span></span>
<span data-ttu-id="89fe2-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89fe2-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89fe2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fe2-129">CommonParameters</span></span>
<span data-ttu-id="89fe2-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89fe2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fe2-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="89fe2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fe2-132">입력</span><span class="sxs-lookup"><span data-stu-id="89fe2-132">INPUTS</span></span>

### <span data-ttu-id="89fe2-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="89fe2-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="89fe2-134">출력</span><span class="sxs-lookup"><span data-stu-id="89fe2-134">OUTPUTS</span></span>

### <span data-ttu-id="89fe2-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="89fe2-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="89fe2-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89fe2-136">NOTES</span></span>

## <span data-ttu-id="89fe2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89fe2-137">RELATED LINKS</span></span>

[<span data-ttu-id="89fe2-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="89fe2-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="89fe2-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="89fe2-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="89fe2-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="89fe2-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="89fe2-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="89fe2-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
