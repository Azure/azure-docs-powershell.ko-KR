---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711301"
---
# <span data-ttu-id="44815-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="44815-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="44815-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44815-102">SYNOPSIS</span></span>
<span data-ttu-id="44815-103">로컬 트래픽 관리자 끝점 개체에 사용자 지정 헤더 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44815-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44815-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44815-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44815-105">DESCRIPTION</span></span>
<span data-ttu-id="44815-106">**Add-AzureRmTrafficManagerCustomHeaderToEndpoint** cmdlet은 사용자 지정 헤더 정보를 로컬 Azure Traffic Manager 끝점 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-106">The **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="44815-107">New-AzureRmTrafficManagerEndpoint 또는 Get-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44815-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="44815-108">이 cmdlet은 로컬 끝점 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="44815-109">Set-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 트래픽 관리자의 끝점에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="44815-110">예제의</span><span class="sxs-lookup"><span data-stu-id="44815-110">EXAMPLES</span></span>

### <span data-ttu-id="44815-111">예제 1: 끝점에 사용자 지정 헤더 정보 추가</span><span class="sxs-lookup"><span data-stu-id="44815-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="44815-112">첫 번째 명령은 **New AzureRmTrafficManagerEndpoint** cmdlet을 사용 하 여 Azure Traffic Manager 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44815-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="44815-113">명령은 로컬 끝점을 $TrafficManagerEndpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="44815-114">두 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에 사용자 지정 헤더 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="44815-115">마지막 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="44815-116">변수</span><span class="sxs-lookup"><span data-stu-id="44815-116">PARAMETERS</span></span>

### <span data-ttu-id="44815-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44815-117">-DefaultProfile</span></span>
<span data-ttu-id="44815-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44815-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44815-119">-이름</span><span class="sxs-lookup"><span data-stu-id="44815-119">-Name</span></span>
<span data-ttu-id="44815-120">추가할 사용자 지정 머리글 정보의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="44815-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44815-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="44815-122">로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="44815-123">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="44815-124">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzureRmTrafficManagerEndpoint 또는 New-AzureRmTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="44815-125">-값</span><span class="sxs-lookup"><span data-stu-id="44815-125">-Value</span></span>
<span data-ttu-id="44815-126">추가할 사용자 지정 헤더 정보의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="44815-127">-확인</span><span class="sxs-lookup"><span data-stu-id="44815-127">-Confirm</span></span>
<span data-ttu-id="44815-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44815-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44815-129">-WhatIf</span></span>
<span data-ttu-id="44815-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44815-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44815-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44815-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44815-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44815-132">CommonParameters</span></span>
<span data-ttu-id="44815-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44815-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44815-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44815-135">입력</span><span class="sxs-lookup"><span data-stu-id="44815-135">INPUTS</span></span>

### <span data-ttu-id="44815-136">TrafficManagerEndpoint (Network.)</span><span class="sxs-lookup"><span data-stu-id="44815-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="44815-137">이 cmdlet은이 cmdlet에 대 한 **TrafficManagerEndpoint** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-137">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="44815-138">출력</span><span class="sxs-lookup"><span data-stu-id="44815-138">OUTPUTS</span></span>

### <span data-ttu-id="44815-139">TrafficManagerEndpoint (Network.)</span><span class="sxs-lookup"><span data-stu-id="44815-139">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="44815-140">이 cmdlet은 수정 된 **TrafficManagerEndpoint** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="44815-140">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="44815-141">상속자</span><span class="sxs-lookup"><span data-stu-id="44815-141">NOTES</span></span>

## <span data-ttu-id="44815-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44815-142">RELATED LINKS</span></span>

[<span data-ttu-id="44815-143">제거-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="44815-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="44815-144">새로운 AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44815-144">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="44815-145">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="44815-145">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="44815-146">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="44815-146">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
