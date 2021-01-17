---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492375"
---
# <span data-ttu-id="bec75-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="bec75-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="bec75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec75-102">SYNOPSIS</span></span>
<span data-ttu-id="bec75-103">SignalR 서비스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="bec75-104">구문</span><span class="sxs-lookup"><span data-stu-id="bec75-104">SYNTAX</span></span>

### <span data-ttu-id="bec75-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bec75-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec75-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bec75-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec75-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bec75-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec75-108">설명</span><span class="sxs-lookup"><span data-stu-id="bec75-108">DESCRIPTION</span></span>
<span data-ttu-id="bec75-109">SignalR 서비스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="bec75-110">예제</span><span class="sxs-lookup"><span data-stu-id="bec75-110">EXAMPLES</span></span>

### <span data-ttu-id="bec75-111">특정 SignalR Service 다시 시작</span><span class="sxs-lookup"><span data-stu-id="bec75-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="bec75-112">기본 리소스 그룹은 \` Set-AzDefault -ResourceGroupName myResourceGroup으로 설정할 수 \` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="bec75-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bec75-113">PARAMETERS</span></span>

### <span data-ttu-id="bec75-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bec75-114">-AsJob</span></span>
<span data-ttu-id="bec75-115">백그라운드 작업에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-115">Run the cmdlet in background job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec75-116">-DefaultProfile</span></span>
<span data-ttu-id="bec75-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec75-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bec75-118">-InputObject</span></span>
<span data-ttu-id="bec75-119">SignalR 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="bec75-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bec75-120">-Name</span></span>
<span data-ttu-id="bec75-121">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="bec75-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bec75-122">-PassThru</span></span>
<span data-ttu-id="bec75-123">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="bec75-123">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec75-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec75-124">-ResourceGroupName</span></span>
<span data-ttu-id="bec75-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-125">The resource group name.</span></span>
<span data-ttu-id="bec75-126">지정하지 않으면 기본 기본 설정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="bec75-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bec75-127">-ResourceId</span></span>
<span data-ttu-id="bec75-128">SignalR Service 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-128">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec75-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bec75-129">-Confirm</span></span>
<span data-ttu-id="bec75-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec75-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec75-131">-WhatIf</span></span>
<span data-ttu-id="bec75-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bec75-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec75-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec75-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec75-134">CommonParameters</span></span>
<span data-ttu-id="bec75-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bec75-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec75-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bec75-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec75-137">입력</span><span class="sxs-lookup"><span data-stu-id="bec75-137">INPUTS</span></span>

### <span data-ttu-id="bec75-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bec75-138">System.String</span></span>

### <span data-ttu-id="bec75-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="bec75-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="bec75-140">출력</span><span class="sxs-lookup"><span data-stu-id="bec75-140">OUTPUTS</span></span>

### <span data-ttu-id="bec75-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bec75-141">System.Boolean</span></span>

## <span data-ttu-id="bec75-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bec75-142">NOTES</span></span>

## <span data-ttu-id="bec75-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bec75-143">RELATED LINKS</span></span>
