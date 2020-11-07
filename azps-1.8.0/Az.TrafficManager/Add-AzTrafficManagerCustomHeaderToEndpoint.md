---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 7e3661a827bb6864fbd43abde43c7ab2bb440ecb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698423"
---
# <span data-ttu-id="0c5d9-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c5d9-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="0c5d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5d9-103">로컬 트래픽 관리자 끝점 개체에 사용자 지정 헤더 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="0c5d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c5d9-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c5d9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5d9-106">**Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet은 사용자 지정 헤더 정보를 로컬 Azure Traffic Manager 끝점 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="0c5d9-107">New-AzTrafficManagerEndpoint 또는 Get-AzTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="0c5d9-108">이 cmdlet은 로컬 끝점 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="0c5d9-109">Set-AzTrafficManagerEndpoint cmdlet을 사용 하 여 트래픽 관리자의 끝점에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="0c5d9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0c5d9-110">EXAMPLES</span></span>

### <span data-ttu-id="0c5d9-111">예제 1: 끝점에 사용자 지정 헤더 정보 추가</span><span class="sxs-lookup"><span data-stu-id="0c5d9-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="0c5d9-112">첫 번째 명령은 **New AzTrafficManagerEndpoint** cmdlet을 사용 하 여 Azure Traffic Manager 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="0c5d9-113">명령은 로컬 끝점을 $TrafficManagerEndpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="0c5d9-114">두 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에 사용자 지정 헤더 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="0c5d9-115">마지막 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="0c5d9-116">변수</span><span class="sxs-lookup"><span data-stu-id="0c5d9-116">PARAMETERS</span></span>

### <span data-ttu-id="0c5d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5d9-117">-DefaultProfile</span></span>
<span data-ttu-id="0c5d9-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c5d9-119">-이름</span><span class="sxs-lookup"><span data-stu-id="0c5d9-119">-Name</span></span>
<span data-ttu-id="0c5d9-120">추가할 사용자 지정 머리글 정보의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="0c5d9-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c5d9-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="0c5d9-122">로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="0c5d9-123">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="0c5d9-124">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzTrafficManagerEndpoint 또는 New-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="0c5d9-125">-값</span><span class="sxs-lookup"><span data-stu-id="0c5d9-125">-Value</span></span>
<span data-ttu-id="0c5d9-126">추가할 사용자 지정 헤더 정보의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="0c5d9-127">-확인</span><span class="sxs-lookup"><span data-stu-id="0c5d9-127">-Confirm</span></span>
<span data-ttu-id="0c5d9-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c5d9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c5d9-129">-WhatIf</span></span>
<span data-ttu-id="0c5d9-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c5d9-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c5d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5d9-132">CommonParameters</span></span>
<span data-ttu-id="0c5d9-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5d9-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c5d9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5d9-135">입력</span><span class="sxs-lookup"><span data-stu-id="0c5d9-135">INPUTS</span></span>

### <span data-ttu-id="0c5d9-136">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0c5d9-137">출력</span><span class="sxs-lookup"><span data-stu-id="0c5d9-137">OUTPUTS</span></span>

### <span data-ttu-id="0c5d9-138">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="0c5d9-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0c5d9-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0c5d9-139">NOTES</span></span>

## <span data-ttu-id="0c5d9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c5d9-140">RELATED LINKS</span></span>

[<span data-ttu-id="0c5d9-141">제거-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c5d9-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="0c5d9-142">새로운 AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c5d9-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0c5d9-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c5d9-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0c5d9-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c5d9-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
