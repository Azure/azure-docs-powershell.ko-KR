---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 075c8e7604ab800e8f1065ff4d025b105d8effc3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871473"
---
# <span data-ttu-id="e72a6-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="e72a6-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="e72a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e72a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e72a6-103">SignalR 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="e72a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e72a6-104">SYNTAX</span></span>

### <span data-ttu-id="e72a6-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e72a6-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e72a6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e72a6-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e72a6-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e72a6-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e72a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e72a6-108">DESCRIPTION</span></span>
<span data-ttu-id="e72a6-109">SignalR 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="e72a6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e72a6-110">EXAMPLES</span></span>

### <span data-ttu-id="e72a6-111">SignalR 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="e72a6-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="e72a6-112">파이프에서 모든 SignalR 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="e72a6-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="e72a6-113">변수</span><span class="sxs-lookup"><span data-stu-id="e72a6-113">PARAMETERS</span></span>

### <span data-ttu-id="e72a6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e72a6-114">-AsJob</span></span>
<span data-ttu-id="e72a6-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e72a6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e72a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72a6-116">-DefaultProfile</span></span>
<span data-ttu-id="e72a6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e72a6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e72a6-118">-InputObject</span></span>
<span data-ttu-id="e72a6-119">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="e72a6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e72a6-120">-Name</span></span>
<span data-ttu-id="e72a6-121">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-121">SignalR service name.</span></span>

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

### <span data-ttu-id="e72a6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e72a6-122">-PassThru</span></span>
<span data-ttu-id="e72a6-123">제거가 성공적으로 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="e72a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e72a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="e72a6-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-125">Resource group name.</span></span>

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

### <span data-ttu-id="e72a6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e72a6-126">-ResourceId</span></span>
<span data-ttu-id="e72a6-127">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="e72a6-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e72a6-128">-Confirm</span></span>
<span data-ttu-id="e72a6-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e72a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e72a6-130">-WhatIf</span></span>
<span data-ttu-id="e72a6-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e72a6-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e72a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72a6-133">CommonParameters</span></span>
<span data-ttu-id="e72a6-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e72a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72a6-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e72a6-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72a6-136">입력</span><span class="sxs-lookup"><span data-stu-id="e72a6-136">INPUTS</span></span>

### <span data-ttu-id="e72a6-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e72a6-137">System.String</span></span>
### <span data-ttu-id="e72a6-138">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="e72a6-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="e72a6-139">출력</span><span class="sxs-lookup"><span data-stu-id="e72a6-139">OUTPUTS</span></span>

### <span data-ttu-id="e72a6-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e72a6-140">System.Boolean</span></span>
## <span data-ttu-id="e72a6-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e72a6-141">NOTES</span></span>

## <span data-ttu-id="e72a6-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e72a6-142">RELATED LINKS</span></span>
