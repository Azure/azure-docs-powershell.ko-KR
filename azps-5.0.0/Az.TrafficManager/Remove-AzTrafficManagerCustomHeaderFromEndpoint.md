---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216311"
---
# <span data-ttu-id="80ac9-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ac9-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="80ac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="80ac9-103">로컬 트래픽 관리자 끝점 개체에서 사용자 지정 헤더 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="80ac9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80ac9-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80ac9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="80ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="80ac9-106">**AzTrafficManagerCustomHeaderFromEndpoint** cmdlet은 로컬 Azure 트래픽 관리자 끝점 개체에서 사용자 지정 헤더 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="80ac9-107">New-AzTrafficManagerEndpoint 또는 Get-AzTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="80ac9-108">이 cmdlet은 로컬 끝점 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="80ac9-109">Set-AzTrafficManagerEndpoint cmdlet을 사용 하 여 트래픽 관리자의 끝점에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="80ac9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="80ac9-110">EXAMPLES</span></span>

### <span data-ttu-id="80ac9-111">예제 1: 끝점에서 사용자 지정 서브넷 정보 제거</span><span class="sxs-lookup"><span data-stu-id="80ac9-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="80ac9-112">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 ContosoProfile 이라는 프로필에서 contoso 라는 Azure 끝점을 가져온 다음 해당 개체를 $TrafficManagerEndpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="80ac9-113">두 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에서 사용자 지정 헤더 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="80ac9-114">마지막 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="80ac9-115">변수</span><span class="sxs-lookup"><span data-stu-id="80ac9-115">PARAMETERS</span></span>

### <span data-ttu-id="80ac9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ac9-116">-DefaultProfile</span></span>
<span data-ttu-id="80ac9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80ac9-118">-이름</span><span class="sxs-lookup"><span data-stu-id="80ac9-118">-Name</span></span>
<span data-ttu-id="80ac9-119">제거할 사용자 지정 머리글 정보의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="80ac9-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ac9-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="80ac9-121">로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="80ac9-122">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="80ac9-123">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzTrafficManagerEndpoint 또는 New-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="80ac9-124">-확인</span><span class="sxs-lookup"><span data-stu-id="80ac9-124">-Confirm</span></span>
<span data-ttu-id="80ac9-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80ac9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80ac9-126">-WhatIf</span></span>
<span data-ttu-id="80ac9-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80ac9-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80ac9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ac9-129">CommonParameters</span></span>
<span data-ttu-id="80ac9-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80ac9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ac9-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80ac9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ac9-132">입력</span><span class="sxs-lookup"><span data-stu-id="80ac9-132">INPUTS</span></span>

### <span data-ttu-id="80ac9-133">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="80ac9-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="80ac9-134">출력</span><span class="sxs-lookup"><span data-stu-id="80ac9-134">OUTPUTS</span></span>

### <span data-ttu-id="80ac9-135">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="80ac9-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="80ac9-136">상속자</span><span class="sxs-lookup"><span data-stu-id="80ac9-136">NOTES</span></span>

## <span data-ttu-id="80ac9-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80ac9-137">RELATED LINKS</span></span>

[<span data-ttu-id="80ac9-138">추가-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ac9-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="80ac9-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="80ac9-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="80ac9-140">새로운 AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ac9-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="80ac9-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ac9-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
