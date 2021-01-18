---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496651"
---
# <span data-ttu-id="6c950-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c950-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="6c950-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c950-102">SYNOPSIS</span></span>
<span data-ttu-id="6c950-103">기존 P2SVpnGateway를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="6c950-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c950-104">SYNTAX</span></span>

### <span data-ttu-id="6c950-105">ByP2SVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6c950-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c950-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6c950-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c950-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6c950-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c950-108">설명</span><span class="sxs-lookup"><span data-stu-id="6c950-108">DESCRIPTION</span></span>
<span data-ttu-id="6c950-109">**Remove-AzP2sVpnGateway** cmdlet을 사용하면 VirtualHub에서 기존 P2SVpnGateway를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="6c950-110">P2SVpnGateway가 제거된 후 모든 지점 및 사이트 클라이언트 연결이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="6c950-111">예제</span><span class="sxs-lookup"><span data-stu-id="6c950-111">EXAMPLES</span></span>

### <span data-ttu-id="6c950-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c950-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="6c950-113">**Remove-AzP2sVpnGateway** cmdlet을 사용하면 VirtualHub에서 기존 P2SVpnGateway를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="6c950-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c950-114">PARAMETERS</span></span>

### <span data-ttu-id="6c950-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c950-115">-DefaultProfile</span></span>
<span data-ttu-id="6c950-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c950-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6c950-117">-Force</span></span>
<span data-ttu-id="6c950-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c950-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c950-119">-InputObject</span></span>
<span data-ttu-id="6c950-120">삭제할 p2sVpnGateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c950-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6c950-121">-Name</span></span>
<span data-ttu-id="6c950-122">P2SVpnGateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c950-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c950-123">-PassThru</span></span>
<span data-ttu-id="6c950-124">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-124">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c950-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c950-125">-ResourceGroupName</span></span>
<span data-ttu-id="6c950-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c950-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c950-127">-ResourceId</span></span>
<span data-ttu-id="6c950-128">삭제할 p2sVpnGateway에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c950-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c950-129">-Confirm</span></span>
<span data-ttu-id="6c950-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c950-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c950-131">-WhatIf</span></span>
<span data-ttu-id="6c950-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6c950-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c950-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c950-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c950-134">CommonParameters</span></span>
<span data-ttu-id="6c950-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c950-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c950-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6c950-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c950-137">입력</span><span class="sxs-lookup"><span data-stu-id="6c950-137">INPUTS</span></span>

### <span data-ttu-id="6c950-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c950-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="6c950-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6c950-139">System.String</span></span>

## <span data-ttu-id="6c950-140">출력</span><span class="sxs-lookup"><span data-stu-id="6c950-140">OUTPUTS</span></span>

### <span data-ttu-id="6c950-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c950-141">System.Boolean</span></span>

## <span data-ttu-id="6c950-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c950-142">NOTES</span></span>

## <span data-ttu-id="6c950-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c950-143">RELATED LINKS</span></span>
