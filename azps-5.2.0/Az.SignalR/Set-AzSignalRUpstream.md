---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338954"
---
# <span data-ttu-id="827cf-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="827cf-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="827cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="827cf-102">SYNOPSIS</span></span>
<span data-ttu-id="827cf-103">SignalR 서비스의 업스트림 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="827cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="827cf-104">SYNTAX</span></span>

### <span data-ttu-id="827cf-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="827cf-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="827cf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="827cf-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="827cf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="827cf-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="827cf-108">설명</span><span class="sxs-lookup"><span data-stu-id="827cf-108">DESCRIPTION</span></span>
<span data-ttu-id="827cf-109">SignalR 서비스의 업스트림 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="827cf-110">예제</span><span class="sxs-lookup"><span data-stu-id="827cf-110">EXAMPLES</span></span>

### <span data-ttu-id="827cf-111">두 개의 순서가 있는 업스트림 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="827cf-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="827cf-112">다음 JSON은 실제 템플릿 집합을 나타내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="827cf-113">모든 업스트림 설정 지우기</span><span class="sxs-lookup"><span data-stu-id="827cf-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="827cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="827cf-114">PARAMETERS</span></span>

### <span data-ttu-id="827cf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="827cf-115">-AsJob</span></span>
<span data-ttu-id="827cf-116">백그라운드 작업에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="827cf-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="827cf-117">-Clear</span></span>
<span data-ttu-id="827cf-118">모든 업스트림 설정을 지우면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="827cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827cf-119">-DefaultProfile</span></span>
<span data-ttu-id="827cf-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="827cf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="827cf-121">-InputObject</span></span>
<span data-ttu-id="827cf-122">SignalR 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="827cf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="827cf-123">-Name</span></span>
<span data-ttu-id="827cf-124">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="827cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="827cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="827cf-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-126">The resource group name.</span></span>
<span data-ttu-id="827cf-127">지정하지 않으면 기본 기본 설정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="827cf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="827cf-128">-ResourceId</span></span>
<span data-ttu-id="827cf-129">SignalR Service 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="827cf-130">-Template</span><span class="sxs-lookup"><span data-stu-id="827cf-130">-Template</span></span>
<span data-ttu-id="827cf-131">업스트림 설정에 대한 템플릿 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="827cf-132">필수 키: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="827cf-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="827cf-133">선택적 키: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="827cf-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="827cf-134">템플릿 매개 변수를 전달하기 위해 Splatting 구문을 사용하는 예제: @{UrlTemplate=' http://host-connections1.com ', HubPattern= 'chat'; EventPattern='broadcast' },@{UrlTemplate=' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="827cf-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="827cf-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="827cf-135">-Confirm</span></span>
<span data-ttu-id="827cf-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="827cf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="827cf-137">-WhatIf</span></span>
<span data-ttu-id="827cf-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="827cf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="827cf-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="827cf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827cf-140">CommonParameters</span></span>
<span data-ttu-id="827cf-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="827cf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827cf-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="827cf-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827cf-143">입력</span><span class="sxs-lookup"><span data-stu-id="827cf-143">INPUTS</span></span>

### <span data-ttu-id="827cf-144">System.String</span><span class="sxs-lookup"><span data-stu-id="827cf-144">System.String</span></span>

## <span data-ttu-id="827cf-145">출력</span><span class="sxs-lookup"><span data-stu-id="827cf-145">OUTPUTS</span></span>

### <span data-ttu-id="827cf-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="827cf-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="827cf-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="827cf-147">NOTES</span></span>

## <span data-ttu-id="827cf-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="827cf-148">RELATED LINKS</span></span>

[<span data-ttu-id="827cf-149">PowerShell에서 Splatting을 사용하여 명령에 매개 변수를 전달하는 방법</span><span class="sxs-lookup"><span data-stu-id="827cf-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
