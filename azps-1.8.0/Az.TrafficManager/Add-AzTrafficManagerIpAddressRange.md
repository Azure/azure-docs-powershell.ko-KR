---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 184b949fa91c7c9993895c8150e21f56244f6e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698417"
---
# <span data-ttu-id="fa985-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="fa985-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="fa985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa985-102">SYNOPSIS</span></span>
<span data-ttu-id="fa985-103">로컬 트래픽 관리자 끝점 개체에 주소 범위 또는 서브넷을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="fa985-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa985-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa985-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fa985-105">DESCRIPTION</span></span>
<span data-ttu-id="fa985-106">**AzTrafficManagerIpAddressRange** cmdlet은 로컬 Azure 트래픽 관리자 끝점 개체에 IP 주소 범위를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="fa985-107">New-AzTrafficManagerEndpoint 또는 Get-AzTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="fa985-108">이 cmdlet은 로컬 끝점 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="fa985-109">Set-AzTrafficManagerEndpoint cmdlet을 사용 하 여 트래픽 관리자의 끝점에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="fa985-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fa985-110">EXAMPLES</span></span>

### <span data-ttu-id="fa985-111">예제 1: 끝점에 IP 주소 범위 추가</span><span class="sxs-lookup"><span data-stu-id="fa985-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="fa985-112">첫 번째 명령은 **New AzTrafficManagerEndpoint** cmdlet을 사용 하 여 Azure Traffic Manager 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="fa985-113">명령은 로컬 끝점을 $TrafficManagerEndpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="fa985-114">두 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에 대 한 IP 주소 범위 1.2.3.4를 5.6.7.8에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="fa985-115">세 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에 9.10.11.255 IP 주소 범위 9.10.11.0를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="fa985-116">네 번째 명령은 범위가 범위 크기와 일치 하는지 확인 한 다음 $TrafficManagerEndpoint에 저장 된 끝점에 대 한 IP 주소 범위 12.13.14.0를 12.13.14.31에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="fa985-117">다섯 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에 15.16.17.18 IP 주소 범위 15.16.17.18를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="fa985-118">마지막 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="fa985-119">변수</span><span class="sxs-lookup"><span data-stu-id="fa985-119">PARAMETERS</span></span>

### <span data-ttu-id="fa985-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa985-120">-DefaultProfile</span></span>
<span data-ttu-id="fa985-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa985-122">-마지막</span><span class="sxs-lookup"><span data-stu-id="fa985-122">-Last</span></span>
<span data-ttu-id="fa985-123">추가할 범위의 마지막 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="fa985-124">-범위</span><span class="sxs-lookup"><span data-stu-id="fa985-124">-Scope</span></span>
<span data-ttu-id="fa985-125">추가할 IP 주소 범위의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-125">Specifies the scope of the IP address range to be added.</span></span>

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

### <span data-ttu-id="fa985-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa985-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="fa985-127">로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="fa985-128">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="fa985-129">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzTrafficManagerEndpoint 또는 New-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="fa985-130">-확인</span><span class="sxs-lookup"><span data-stu-id="fa985-130">-Confirm</span></span>
<span data-ttu-id="fa985-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa985-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa985-132">-WhatIf</span></span>
<span data-ttu-id="fa985-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa985-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa985-135">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="fa985-135">-First</span></span>
<span data-ttu-id="fa985-136">추가할 범위의 첫 번째 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="fa985-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa985-137">CommonParameters</span></span>
<span data-ttu-id="fa985-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa985-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa985-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa985-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa985-140">입력</span><span class="sxs-lookup"><span data-stu-id="fa985-140">INPUTS</span></span>

### <span data-ttu-id="fa985-141">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="fa985-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="fa985-142">출력</span><span class="sxs-lookup"><span data-stu-id="fa985-142">OUTPUTS</span></span>

### <span data-ttu-id="fa985-143">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="fa985-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="fa985-144">상속자</span><span class="sxs-lookup"><span data-stu-id="fa985-144">NOTES</span></span>

## <span data-ttu-id="fa985-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa985-145">RELATED LINKS</span></span>

[<span data-ttu-id="fa985-146">제거-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="fa985-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="fa985-147">새로운 AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa985-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fa985-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fa985-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fa985-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa985-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
