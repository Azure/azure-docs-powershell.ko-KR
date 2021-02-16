---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: ec1bba32027d3ec96aef61f3abec7d51cec5c35b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184433"
---
# <span data-ttu-id="6a360-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="6a360-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="6a360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a360-102">SYNOPSIS</span></span>
<span data-ttu-id="6a360-103">연결 모니터 출력 대상 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a360-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="6a360-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a360-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a360-105">설명</span><span class="sxs-lookup"><span data-stu-id="6a360-105">DESCRIPTION</span></span>
<span data-ttu-id="6a360-106">New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet은 연결 모니터 출력 대상 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a360-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="6a360-107">예제</span><span class="sxs-lookup"><span data-stu-id="6a360-107">EXAMPLES</span></span>

### <span data-ttu-id="6a360-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a360-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="6a360-109">형식 : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="6a360-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="6a360-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a360-110">PARAMETERS</span></span>

### <span data-ttu-id="6a360-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a360-111">-DefaultProfile</span></span>
<span data-ttu-id="6a360-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a360-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a360-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="6a360-113">-OutputType</span></span>
<span data-ttu-id="6a360-114">연결 모니터 출력 대상 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6a360-114">Connection monitor output destination type.</span></span> <span data-ttu-id="6a360-115">현재는 작업 \" 영역만 \" 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a360-115">Currently, only \"Workspace\" is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a360-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="6a360-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="6a360-117">Log Analytics 작업 영역 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a360-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="6a360-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a360-118">-Confirm</span></span>
<span data-ttu-id="6a360-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a360-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a360-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a360-120">-WhatIf</span></span>
<span data-ttu-id="6a360-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6a360-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a360-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a360-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a360-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a360-123">CommonParameters</span></span>
<span data-ttu-id="6a360-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a360-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a360-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a360-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a360-126">입력</span><span class="sxs-lookup"><span data-stu-id="6a360-126">INPUTS</span></span>

### <span data-ttu-id="6a360-127">없음</span><span class="sxs-lookup"><span data-stu-id="6a360-127">None</span></span>

## <span data-ttu-id="6a360-128">출력</span><span class="sxs-lookup"><span data-stu-id="6a360-128">OUTPUTS</span></span>

### <span data-ttu-id="6a360-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="6a360-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="6a360-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a360-130">NOTES</span></span>

## <span data-ttu-id="6a360-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a360-131">RELATED LINKS</span></span>
