---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492733"
---
# <span data-ttu-id="7f66e-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f66e-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="7f66e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f66e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f66e-103">로컬 Traffic Manager 엔드포인트 개체에 사용자 지정 헤더 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="7f66e-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f66e-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f66e-105">설명</span><span class="sxs-lookup"><span data-stu-id="7f66e-105">DESCRIPTION</span></span>
<span data-ttu-id="7f66e-106">**Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet은 로컬 Azure Traffic Manager 엔드포인트 개체에 사용자 지정 헤더 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="7f66e-107">New-AzTrafficManagerEndpoint cmdlet을 사용하여 엔드포인트를 Get-AzTrafficManagerEndpoint 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="7f66e-108">이 cmdlet은 로컬 엔드포인트 개체에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="7f66e-109">Set-AzTrafficManagerEndpoint cmdlet을 사용하여 Traffic Manager에 대한 엔드포인트에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="7f66e-110">예제</span><span class="sxs-lookup"><span data-stu-id="7f66e-110">EXAMPLES</span></span>

### <span data-ttu-id="7f66e-111">예제 1: 엔드포인트에 사용자 지정 헤더 정보 추가</span><span class="sxs-lookup"><span data-stu-id="7f66e-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="7f66e-112">첫 번째 명령은 **New-AzTrafficManagerEndpoint** cmdlet을 사용하여 Azure Traffic Manager 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="7f66e-113">이 명령은 로컬 엔드포인트를 $TrafficManagerEndpoint 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="7f66e-114">두 번째 명령은 사용자 지정 헤더 정보를 사용자 지정 헤더에 저장된 엔드포인트에 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7f66e-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="7f66e-115">마지막 명령은 Traffic Manager의 엔드포인트를 업데이트하여 트래픽 관리자의 로컬 값과 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7f66e-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="7f66e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f66e-116">PARAMETERS</span></span>

### <span data-ttu-id="7f66e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f66e-117">-DefaultProfile</span></span>
<span data-ttu-id="7f66e-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f66e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7f66e-119">-Name</span></span>
<span data-ttu-id="7f66e-120">추가할 사용자 지정 헤더 정보의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="7f66e-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f66e-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="7f66e-122">로컬 **TrafficManagerEndpoint 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="7f66e-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="7f66e-123">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="7f66e-124">**TrafficManagerEndpoint** 개체를 얻습니다. Get-AzTrafficManagerEndpoint 또는 New-AzTrafficManagerEndpoint 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="7f66e-125">-Value</span><span class="sxs-lookup"><span data-stu-id="7f66e-125">-Value</span></span>
<span data-ttu-id="7f66e-126">추가할 사용자 지정 헤더 정보의 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="7f66e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f66e-127">-Confirm</span></span>
<span data-ttu-id="7f66e-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f66e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f66e-129">-WhatIf</span></span>
<span data-ttu-id="7f66e-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7f66e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f66e-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f66e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f66e-132">CommonParameters</span></span>
<span data-ttu-id="7f66e-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f66e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f66e-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7f66e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f66e-135">입력</span><span class="sxs-lookup"><span data-stu-id="7f66e-135">INPUTS</span></span>

### <span data-ttu-id="7f66e-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f66e-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7f66e-137">출력</span><span class="sxs-lookup"><span data-stu-id="7f66e-137">OUTPUTS</span></span>

### <span data-ttu-id="7f66e-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f66e-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7f66e-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f66e-139">NOTES</span></span>

## <span data-ttu-id="7f66e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f66e-140">RELATED LINKS</span></span>

[<span data-ttu-id="7f66e-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f66e-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="7f66e-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f66e-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7f66e-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7f66e-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7f66e-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f66e-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
