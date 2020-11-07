---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 6096bb59622e873d100752646ae6c101b43923e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699087"
---
# <span data-ttu-id="6ca92-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="6ca92-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="6ca92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ca92-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca92-103">SignalR 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="6ca92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ca92-104">SYNTAX</span></span>

### <span data-ttu-id="6ca92-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ca92-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca92-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca92-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca92-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca92-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca92-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6ca92-108">DESCRIPTION</span></span>
<span data-ttu-id="6ca92-109">SignalR 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="6ca92-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ca92-110">EXAMPLES</span></span>

### <span data-ttu-id="6ca92-111">SignalR 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="6ca92-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="6ca92-112">파이프에서 모든 SignalR 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="6ca92-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="6ca92-113">변수</span><span class="sxs-lookup"><span data-stu-id="6ca92-113">PARAMETERS</span></span>

### <span data-ttu-id="6ca92-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ca92-114">-AsJob</span></span>
<span data-ttu-id="6ca92-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6ca92-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ca92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca92-116">-DefaultProfile</span></span>
<span data-ttu-id="6ca92-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca92-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ca92-118">-InputObject</span></span>
<span data-ttu-id="6ca92-119">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="6ca92-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6ca92-120">-Name</span></span>
<span data-ttu-id="6ca92-121">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-121">SignalR service name.</span></span>

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

### <span data-ttu-id="6ca92-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ca92-122">-PassThru</span></span>
<span data-ttu-id="6ca92-123">제거가 성공적으로 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="6ca92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca92-124">-ResourceGroupName</span></span>
<span data-ttu-id="6ca92-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-125">Resource group name.</span></span>

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

### <span data-ttu-id="6ca92-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca92-126">-ResourceId</span></span>
<span data-ttu-id="6ca92-127">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="6ca92-128">-확인</span><span class="sxs-lookup"><span data-stu-id="6ca92-128">-Confirm</span></span>
<span data-ttu-id="6ca92-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca92-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca92-130">-WhatIf</span></span>
<span data-ttu-id="6ca92-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca92-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca92-133">CommonParameters</span></span>
<span data-ttu-id="6ca92-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca92-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca92-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca92-136">입력</span><span class="sxs-lookup"><span data-stu-id="6ca92-136">INPUTS</span></span>

### <span data-ttu-id="6ca92-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ca92-137">System.String</span></span>

### <span data-ttu-id="6ca92-138">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="6ca92-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="6ca92-139">출력</span><span class="sxs-lookup"><span data-stu-id="6ca92-139">OUTPUTS</span></span>

### <span data-ttu-id="6ca92-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6ca92-140">System.Boolean</span></span>

## <span data-ttu-id="6ca92-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6ca92-141">NOTES</span></span>

## <span data-ttu-id="6ca92-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ca92-142">RELATED LINKS</span></span>