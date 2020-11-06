---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525927"
---
# <span data-ttu-id="bebbe-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="bebbe-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="bebbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bebbe-102">SYNOPSIS</span></span>
<span data-ttu-id="bebbe-103">로컬 트래픽 관리자 끝점 개체에서 사용자 지정 헤더 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bebbe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bebbe-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bebbe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bebbe-105">DESCRIPTION</span></span>
<span data-ttu-id="bebbe-106">**AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet은 로컬 Azure 트래픽 관리자 끝점 개체에서 사용자 지정 헤더 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="bebbe-107">New-AzureRmTrafficManagerEndpoint 또는 Get-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="bebbe-108">이 cmdlet은 로컬 끝점 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="bebbe-109">Set-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 트래픽 관리자의 끝점에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="bebbe-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bebbe-110">EXAMPLES</span></span>

### <span data-ttu-id="bebbe-111">예제 1: 끝점에서 사용자 지정 서브넷 정보 제거</span><span class="sxs-lookup"><span data-stu-id="bebbe-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="bebbe-112">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 ContosoProfile 이라는 프로필에서 contoso 라는 Azure 끝점을 가져온 다음 해당 개체를 $TrafficManagerEndpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="bebbe-113">두 번째 명령은 $TrafficManagerEndpoint에 저장 된 끝점에서 사용자 지정 헤더 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="bebbe-114">마지막 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="bebbe-115">변수</span><span class="sxs-lookup"><span data-stu-id="bebbe-115">PARAMETERS</span></span>

### <span data-ttu-id="bebbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bebbe-116">-DefaultProfile</span></span>
<span data-ttu-id="bebbe-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bebbe-118">-이름</span><span class="sxs-lookup"><span data-stu-id="bebbe-118">-Name</span></span>
<span data-ttu-id="bebbe-119">제거할 사용자 지정 머리글 정보의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="bebbe-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bebbe-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="bebbe-121">로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="bebbe-122">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="bebbe-123">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzureRmTrafficManagerEndpoint 또는 New-AzureRmTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="bebbe-124">-확인</span><span class="sxs-lookup"><span data-stu-id="bebbe-124">-Confirm</span></span>
<span data-ttu-id="bebbe-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bebbe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bebbe-126">-WhatIf</span></span>
<span data-ttu-id="bebbe-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bebbe-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bebbe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bebbe-129">CommonParameters</span></span>
<span data-ttu-id="bebbe-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bebbe-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bebbe-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bebbe-132">입력</span><span class="sxs-lookup"><span data-stu-id="bebbe-132">INPUTS</span></span>

### <span data-ttu-id="bebbe-133">TrafficManagerEndpoint (Network.)</span><span class="sxs-lookup"><span data-stu-id="bebbe-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="bebbe-134">이 cmdlet은이 cmdlet에 대 한 **TrafficManagerEndpoint** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="bebbe-135">출력</span><span class="sxs-lookup"><span data-stu-id="bebbe-135">OUTPUTS</span></span>

### <span data-ttu-id="bebbe-136">TrafficManagerEndpoint (Network.)</span><span class="sxs-lookup"><span data-stu-id="bebbe-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="bebbe-137">이 cmdlet은 수정 된 TrafficManagerEndpoint 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bebbe-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="bebbe-138">상속자</span><span class="sxs-lookup"><span data-stu-id="bebbe-138">NOTES</span></span>

## <span data-ttu-id="bebbe-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bebbe-139">RELATED LINKS</span></span>

[<span data-ttu-id="bebbe-140">추가-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="bebbe-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="bebbe-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bebbe-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="bebbe-142">새로운 AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bebbe-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="bebbe-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bebbe-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
