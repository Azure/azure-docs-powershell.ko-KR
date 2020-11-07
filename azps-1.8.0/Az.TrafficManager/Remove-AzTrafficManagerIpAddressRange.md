---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: ea69e8d07278be2c9f122d179090e63b9153128d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698385"
---
# <span data-ttu-id="aed21-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="aed21-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="aed21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aed21-102">SYNOPSIS</span></span>
<span data-ttu-id="aed21-103">로컬 트래픽 관리자 끝점 개체에서 주소 범위 또는 서브넷을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="aed21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aed21-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aed21-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aed21-105">DESCRIPTION</span></span>
<span data-ttu-id="aed21-106">**AzTrafficManagerIpAddressRange** cmdlet은 로컬 Azure 트래픽 관리자 끝점 개체에서 IP 주소 범위를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="aed21-107">New-AzTrafficManagerEndpoint 또는 Get-AzTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="aed21-108">이 cmdlet은 로컬 끝점 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="aed21-109">Set-AzTrafficManagerEndpoint cmdlet을 사용 하 여 트래픽 관리자의 끝점에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="aed21-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aed21-110">EXAMPLES</span></span>

### <span data-ttu-id="aed21-111">예제 1: 끝점에서 IP 주소 범위 제거</span><span class="sxs-lookup"><span data-stu-id="aed21-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="aed21-112">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 ContosoProfile 이라는 프로필에서 contoso 라는 Azure 끝점을 가져온 다음 해당 개체를 $TrafficManagerEndpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="aed21-113">두 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에서 IP 주소 범위를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="aed21-114">마지막 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="aed21-115">변수</span><span class="sxs-lookup"><span data-stu-id="aed21-115">PARAMETERS</span></span>

### <span data-ttu-id="aed21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed21-116">-DefaultProfile</span></span>
<span data-ttu-id="aed21-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed21-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aed21-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="aed21-119">로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="aed21-120">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="aed21-121">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzTrafficManagerEndpoint 또는 New-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="aed21-122">-확인</span><span class="sxs-lookup"><span data-stu-id="aed21-122">-Confirm</span></span>
<span data-ttu-id="aed21-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aed21-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aed21-124">-WhatIf</span></span>
<span data-ttu-id="aed21-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aed21-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aed21-127">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="aed21-127">-First</span></span>
<span data-ttu-id="aed21-128">제거할 범위의 첫 번째 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="aed21-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed21-129">CommonParameters</span></span>
<span data-ttu-id="aed21-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed21-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed21-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed21-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed21-132">입력</span><span class="sxs-lookup"><span data-stu-id="aed21-132">INPUTS</span></span>

### <span data-ttu-id="aed21-133">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="aed21-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="aed21-134">출력</span><span class="sxs-lookup"><span data-stu-id="aed21-134">OUTPUTS</span></span>

### <span data-ttu-id="aed21-135">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="aed21-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="aed21-136">상속자</span><span class="sxs-lookup"><span data-stu-id="aed21-136">NOTES</span></span>

## <span data-ttu-id="aed21-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aed21-137">RELATED LINKS</span></span>

[<span data-ttu-id="aed21-138">추가-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="aed21-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="aed21-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aed21-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="aed21-140">새로운 AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aed21-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="aed21-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aed21-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
