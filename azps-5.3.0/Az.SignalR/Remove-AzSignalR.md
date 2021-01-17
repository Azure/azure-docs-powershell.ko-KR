---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491626"
---
# <span data-ttu-id="c98a7-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="c98a7-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="c98a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c98a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c98a7-103">SignalR 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="c98a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="c98a7-104">SYNTAX</span></span>

### <span data-ttu-id="c98a7-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c98a7-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c98a7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c98a7-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c98a7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c98a7-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c98a7-108">설명</span><span class="sxs-lookup"><span data-stu-id="c98a7-108">DESCRIPTION</span></span>
<span data-ttu-id="c98a7-109">SignalR 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="c98a7-110">예제</span><span class="sxs-lookup"><span data-stu-id="c98a7-110">EXAMPLES</span></span>

### <span data-ttu-id="c98a7-111">SignalR Service 제거</span><span class="sxs-lookup"><span data-stu-id="c98a7-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="c98a7-112">파이프에서 모든 SignalR Service 제거</span><span class="sxs-lookup"><span data-stu-id="c98a7-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="c98a7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c98a7-113">PARAMETERS</span></span>

### <span data-ttu-id="c98a7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c98a7-114">-AsJob</span></span>
<span data-ttu-id="c98a7-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c98a7-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98a7-116">-DefaultProfile</span></span>
<span data-ttu-id="c98a7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c98a7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c98a7-118">-InputObject</span></span>
<span data-ttu-id="c98a7-119">SignalR 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-119">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c98a7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c98a7-120">-Name</span></span>
<span data-ttu-id="c98a7-121">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-121">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c98a7-122">-PassThru</span></span>
<span data-ttu-id="c98a7-123">제거가 성공적으로 완료되면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c98a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="c98a7-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c98a7-126">-ResourceId</span></span>
<span data-ttu-id="c98a7-127">SignalR Service 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-127">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c98a7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c98a7-128">-Confirm</span></span>
<span data-ttu-id="c98a7-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c98a7-130">-WhatIf</span></span>
<span data-ttu-id="c98a7-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c98a7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c98a7-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98a7-133">CommonParameters</span></span>
<span data-ttu-id="c98a7-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c98a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98a7-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c98a7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98a7-136">입력</span><span class="sxs-lookup"><span data-stu-id="c98a7-136">INPUTS</span></span>

### <span data-ttu-id="c98a7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c98a7-137">System.String</span></span>
### <span data-ttu-id="c98a7-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c98a7-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="c98a7-139">출력</span><span class="sxs-lookup"><span data-stu-id="c98a7-139">OUTPUTS</span></span>

### <span data-ttu-id="c98a7-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c98a7-140">System.Boolean</span></span>
## <span data-ttu-id="c98a7-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c98a7-141">NOTES</span></span>

## <span data-ttu-id="c98a7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c98a7-142">RELATED LINKS</span></span>
