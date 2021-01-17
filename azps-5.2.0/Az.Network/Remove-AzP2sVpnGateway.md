---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328033"
---
# <span data-ttu-id="a3416-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3416-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="a3416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3416-102">SYNOPSIS</span></span>
<span data-ttu-id="a3416-103">기존 P2SVpnGateway를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="a3416-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3416-104">SYNTAX</span></span>

### <span data-ttu-id="a3416-105">ByP2SVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a3416-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3416-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a3416-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3416-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a3416-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3416-108">설명</span><span class="sxs-lookup"><span data-stu-id="a3416-108">DESCRIPTION</span></span>
<span data-ttu-id="a3416-109">**Remove-AzP2sVpnGateway** cmdlet을 사용하면 VirtualHub에서 기존 P2SVpnGateway를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="a3416-110">P2SVpnGateway가 제거된 후 모든 지점 및 사이트 클라이언트 연결이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="a3416-111">예제</span><span class="sxs-lookup"><span data-stu-id="a3416-111">EXAMPLES</span></span>

### <span data-ttu-id="a3416-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3416-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="a3416-113">**Remove-AzP2sVpnGateway** cmdlet을 사용하면 VirtualHub에서 기존 P2SVpnGateway를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="a3416-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3416-114">PARAMETERS</span></span>

### <span data-ttu-id="a3416-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3416-115">-DefaultProfile</span></span>
<span data-ttu-id="a3416-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3416-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a3416-117">-Force</span></span>
<span data-ttu-id="a3416-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a3416-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3416-119">-InputObject</span></span>
<span data-ttu-id="a3416-120">삭제할 p2sVpnGateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-120">The p2sVpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="a3416-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a3416-121">-Name</span></span>
<span data-ttu-id="a3416-122">P2SVpnGateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-122">The P2SVpnGateway name.</span></span>

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

### <span data-ttu-id="a3416-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3416-123">-PassThru</span></span>
<span data-ttu-id="a3416-124">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="a3416-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3416-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3416-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-126">The resource group name.</span></span>

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

### <span data-ttu-id="a3416-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3416-127">-ResourceId</span></span>
<span data-ttu-id="a3416-128">삭제할 p2sVpnGateway에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="a3416-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3416-129">-Confirm</span></span>
<span data-ttu-id="a3416-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3416-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3416-131">-WhatIf</span></span>
<span data-ttu-id="a3416-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a3416-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3416-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3416-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3416-134">CommonParameters</span></span>
<span data-ttu-id="a3416-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3416-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3416-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a3416-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3416-137">입력</span><span class="sxs-lookup"><span data-stu-id="a3416-137">INPUTS</span></span>

### <span data-ttu-id="a3416-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a3416-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="a3416-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a3416-139">System.String</span></span>

## <span data-ttu-id="a3416-140">출력</span><span class="sxs-lookup"><span data-stu-id="a3416-140">OUTPUTS</span></span>

### <span data-ttu-id="a3416-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3416-141">System.Boolean</span></span>

## <span data-ttu-id="a3416-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3416-142">NOTES</span></span>

## <span data-ttu-id="a3416-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3416-143">RELATED LINKS</span></span>
