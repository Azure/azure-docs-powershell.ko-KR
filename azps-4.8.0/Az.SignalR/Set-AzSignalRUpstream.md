---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056985"
---
# <span data-ttu-id="f732c-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="f732c-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="f732c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f732c-102">SYNOPSIS</span></span>
<span data-ttu-id="f732c-103">SignalR 서비스의 업스트림 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="f732c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f732c-104">SYNTAX</span></span>

### <span data-ttu-id="f732c-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f732c-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f732c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f732c-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f732c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f732c-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f732c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f732c-108">DESCRIPTION</span></span>
<span data-ttu-id="f732c-109">SignalR 서비스의 업스트림 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="f732c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f732c-110">EXAMPLES</span></span>

### <span data-ttu-id="f732c-111">두 개의 순서가 지정 된 업스트림 서식 파일 설정</span><span class="sxs-lookup"><span data-stu-id="f732c-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="f732c-112">다음 JSON은 실제 서식 파일 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-112">The following JSON represents the actual templates set.</span></span> 

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

### <span data-ttu-id="f732c-113">모든 업스트림 설정 지우기</span><span class="sxs-lookup"><span data-stu-id="f732c-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="f732c-114">변수</span><span class="sxs-lookup"><span data-stu-id="f732c-114">PARAMETERS</span></span>

### <span data-ttu-id="f732c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f732c-115">-AsJob</span></span>
<span data-ttu-id="f732c-116">백그라운드 작업에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="f732c-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="f732c-117">-Clear</span></span>
<span data-ttu-id="f732c-118">모든 업스트림 설정을 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="f732c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f732c-119">-DefaultProfile</span></span>
<span data-ttu-id="f732c-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f732c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f732c-121">-InputObject</span></span>
<span data-ttu-id="f732c-122">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="f732c-123">-이름</span><span class="sxs-lookup"><span data-stu-id="f732c-123">-Name</span></span>
<span data-ttu-id="f732c-124">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="f732c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f732c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f732c-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-126">The resource group name.</span></span>
<span data-ttu-id="f732c-127">지정 되지 않은 경우 기본 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="f732c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f732c-128">-ResourceId</span></span>
<span data-ttu-id="f732c-129">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="f732c-130">-Template</span><span class="sxs-lookup"><span data-stu-id="f732c-130">-Template</span></span>
<span data-ttu-id="f732c-131">업스트림 설정에 대 한 템플릿 항목</span><span class="sxs-lookup"><span data-stu-id="f732c-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="f732c-132">필수 키: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="f732c-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="f732c-133">선택적 키: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="f732c-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="f732c-134">Splatting 구문을 사용 하 여 template 매개 변수를 전달 하는 예: @ {UrlTemplate = ' http://host-connections1.com ', HubPattern = ' 채팅 '; EventPattern = ' 브로드캐스트 '}, @ {UrlTemplate = ' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="f732c-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

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

### <span data-ttu-id="f732c-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f732c-135">-Confirm</span></span>
<span data-ttu-id="f732c-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f732c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f732c-137">-WhatIf</span></span>
<span data-ttu-id="f732c-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f732c-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f732c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f732c-140">CommonParameters</span></span>
<span data-ttu-id="f732c-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f732c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f732c-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f732c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f732c-143">입력</span><span class="sxs-lookup"><span data-stu-id="f732c-143">INPUTS</span></span>

### <span data-ttu-id="f732c-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f732c-144">System.String</span></span>

## <span data-ttu-id="f732c-145">출력</span><span class="sxs-lookup"><span data-stu-id="f732c-145">OUTPUTS</span></span>

### <span data-ttu-id="f732c-146">SignalR. PSServerlessUpstreamSettings/.</span><span class="sxs-lookup"><span data-stu-id="f732c-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="f732c-147">상속자</span><span class="sxs-lookup"><span data-stu-id="f732c-147">NOTES</span></span>

## <span data-ttu-id="f732c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f732c-148">RELATED LINKS</span></span>

[<span data-ttu-id="f732c-149">Splatting를 사용 하 여 PowerShell의 명령에 매개 변수를 전달 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f732c-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
