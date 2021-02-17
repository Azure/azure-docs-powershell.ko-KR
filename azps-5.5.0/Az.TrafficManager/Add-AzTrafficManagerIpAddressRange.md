---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198316"
---
# <span data-ttu-id="56967-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="56967-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="56967-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56967-102">SYNOPSIS</span></span>
<span data-ttu-id="56967-103">주소 범위 또는 서브넷을 로컬 Traffic Manager 엔드포인트 개체에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="56967-104">구문</span><span class="sxs-lookup"><span data-stu-id="56967-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56967-105">설명</span><span class="sxs-lookup"><span data-stu-id="56967-105">DESCRIPTION</span></span>
<span data-ttu-id="56967-106">**Add-AzTrafficManagerIpAddressRange** cmdlet은 로컬 Azure Traffic Manager 엔드포인트 개체에 IP 주소 범위를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="56967-107">New-AzTrafficManagerEndpoint cmdlet을 사용하여 엔드포인트를 Get-AzTrafficManagerEndpoint 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56967-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="56967-108">이 cmdlet은 로컬 엔드포인트 개체에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="56967-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="56967-109">다음 cmdlet을 사용하여 Traffic Manager에 대한 변경 내용을 Set-AzTrafficManagerEndpoint 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="56967-110">예제</span><span class="sxs-lookup"><span data-stu-id="56967-110">EXAMPLES</span></span>

### <span data-ttu-id="56967-111">예제 1: 엔드포인트에 IP 주소 범위 추가</span><span class="sxs-lookup"><span data-stu-id="56967-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="56967-112">첫 번째 명령은 **New-AzTrafficManagerEndpoint** cmdlet을 사용하여 Azure Traffic Manager 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56967-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="56967-113">이 명령은 로컬 엔드포인트를 $TrafficManagerEndpoint 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="56967-114">두 번째 명령은 IP 주소 범위 1.2.3.4~5.6.7.8을 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56967-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="56967-115">세 번째 명령은 IP 주소 범위 9.10.11.0~9.10.11.255를 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56967-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="56967-116">네 번째 명령은 범위가 범위의 크기와 일치하는지 확인한 다음 IP 주소 범위 12.13.14.0~12.13.14.31을 해당 범위에 저장된 엔드포인트에 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56967-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="56967-117">다섯 번째 명령은 IP 주소 범위 15.16.17.18~15.16.17.18을 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56967-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="56967-118">마지막 명령은 Traffic Manager의 엔드포인트를 업데이트하여 트래픽 관리자의 로컬 값과 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56967-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="56967-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56967-119">PARAMETERS</span></span>

### <span data-ttu-id="56967-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56967-120">-DefaultProfile</span></span>
<span data-ttu-id="56967-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56967-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56967-122">-Last</span><span class="sxs-lookup"><span data-stu-id="56967-122">-Last</span></span>
<span data-ttu-id="56967-123">추가할 범위의 마지막 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-123">Specifies the last IP address in the range to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56967-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="56967-124">-Scope</span></span>
<span data-ttu-id="56967-125">추가할 IP 주소 범위의 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56967-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56967-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="56967-127">로컬 **TrafficManagerEndpoint 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="56967-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="56967-128">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="56967-129">**TrafficManagerEndpoint** 개체를 얻습니다. Get-AzTrafficManagerEndpoint 또는 New-AzTrafficManagerEndpoint 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="56967-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56967-130">-Confirm</span></span>
<span data-ttu-id="56967-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="56967-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56967-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56967-132">-WhatIf</span></span>
<span data-ttu-id="56967-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="56967-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56967-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56967-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56967-135">-First</span><span class="sxs-lookup"><span data-stu-id="56967-135">-First</span></span>
<span data-ttu-id="56967-136">추가할 범위의 첫 번째 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="56967-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56967-137">CommonParameters</span></span>
<span data-ttu-id="56967-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56967-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56967-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="56967-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56967-140">입력</span><span class="sxs-lookup"><span data-stu-id="56967-140">INPUTS</span></span>

### <span data-ttu-id="56967-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56967-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="56967-142">출력</span><span class="sxs-lookup"><span data-stu-id="56967-142">OUTPUTS</span></span>

### <span data-ttu-id="56967-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56967-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="56967-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56967-144">NOTES</span></span>

## <span data-ttu-id="56967-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56967-145">RELATED LINKS</span></span>

[<span data-ttu-id="56967-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="56967-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="56967-147">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56967-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="56967-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56967-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="56967-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56967-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
