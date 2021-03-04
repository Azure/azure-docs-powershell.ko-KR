---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: c98b716f37fcf9aafafacdefad4c51b0451cf12d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955456"
---
# <span data-ttu-id="d1574-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="d1574-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="d1574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1574-102">SYNOPSIS</span></span>
<span data-ttu-id="d1574-103">SignalR 서비스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="d1574-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1574-104">SYNTAX</span></span>

### <span data-ttu-id="d1574-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d1574-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1574-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1574-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1574-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1574-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1574-108">설명</span><span class="sxs-lookup"><span data-stu-id="d1574-108">DESCRIPTION</span></span>
<span data-ttu-id="d1574-109">SignalR 서비스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="d1574-110">예제</span><span class="sxs-lookup"><span data-stu-id="d1574-110">EXAMPLES</span></span>

### <span data-ttu-id="d1574-111">특정 SignalR 서비스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="d1574-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="d1574-112">기본 리소스 그룹은 \` Set-AzDefault -ResourceGroupName myResourceGroup 로 설정할 수 \` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="d1574-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1574-113">PARAMETERS</span></span>

### <span data-ttu-id="d1574-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1574-114">-AsJob</span></span>
<span data-ttu-id="d1574-115">백그라운드 작업에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="d1574-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1574-116">-DefaultProfile</span></span>
<span data-ttu-id="d1574-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1574-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1574-118">-InputObject</span></span>
<span data-ttu-id="d1574-119">SignalR 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d1574-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d1574-120">-Name</span></span>
<span data-ttu-id="d1574-121">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="d1574-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1574-122">-PassThru</span></span>
<span data-ttu-id="d1574-123">{{ Fill PassThru 설명 }}</span><span class="sxs-lookup"><span data-stu-id="d1574-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d1574-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1574-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1574-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-125">The resource group name.</span></span>
<span data-ttu-id="d1574-126">지정하지 않은 경우 기본 설정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="d1574-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1574-127">-ResourceId</span></span>
<span data-ttu-id="d1574-128">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d1574-129">-확인</span><span class="sxs-lookup"><span data-stu-id="d1574-129">-Confirm</span></span>
<span data-ttu-id="d1574-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1574-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1574-131">-WhatIf</span></span>
<span data-ttu-id="d1574-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1574-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1574-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1574-134">CommonParameters</span></span>
<span data-ttu-id="d1574-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1574-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1574-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1574-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1574-137">입력</span><span class="sxs-lookup"><span data-stu-id="d1574-137">INPUTS</span></span>

### <span data-ttu-id="d1574-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d1574-138">System.String</span></span>

### <span data-ttu-id="d1574-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d1574-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="d1574-140">출력</span><span class="sxs-lookup"><span data-stu-id="d1574-140">OUTPUTS</span></span>

### <span data-ttu-id="d1574-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1574-141">System.Boolean</span></span>

## <span data-ttu-id="d1574-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1574-142">NOTES</span></span>

## <span data-ttu-id="d1574-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1574-143">RELATED LINKS</span></span>
