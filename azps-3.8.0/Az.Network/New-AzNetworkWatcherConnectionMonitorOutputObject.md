---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034482"
---
# <span data-ttu-id="60e10-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="60e10-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="60e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60e10-102">SYNOPSIS</span></span>
<span data-ttu-id="60e10-103">연결 모니터 출력 대상 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="60e10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60e10-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e10-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60e10-105">DESCRIPTION</span></span>
<span data-ttu-id="60e10-106">New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet은 연결 모니터 출력 대상 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="60e10-107">예제의</span><span class="sxs-lookup"><span data-stu-id="60e10-107">EXAMPLES</span></span>

### <span data-ttu-id="60e10-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="60e10-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="60e10-109">유형: "workspace" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="60e10-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="60e10-110">변수</span><span class="sxs-lookup"><span data-stu-id="60e10-110">PARAMETERS</span></span>

### <span data-ttu-id="60e10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e10-111">-DefaultProfile</span></span>
<span data-ttu-id="60e10-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e10-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="60e10-113">-OutputType</span></span>
<span data-ttu-id="60e10-114">연결 모니터 출력 대상 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-114">Connection monitor output destination type.</span></span> <span data-ttu-id="60e10-115">현재 \" 작업 영역만 \" 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="60e10-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="60e10-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="60e10-117">로그 분석 작업 영역 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="60e10-118">-확인</span><span class="sxs-lookup"><span data-stu-id="60e10-118">-Confirm</span></span>
<span data-ttu-id="60e10-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e10-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e10-120">-WhatIf</span></span>
<span data-ttu-id="60e10-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60e10-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60e10-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e10-123">CommonParameters</span></span>
<span data-ttu-id="60e10-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60e10-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e10-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="60e10-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e10-126">입력</span><span class="sxs-lookup"><span data-stu-id="60e10-126">INPUTS</span></span>

### <span data-ttu-id="60e10-127">않아야</span><span class="sxs-lookup"><span data-stu-id="60e10-127">None</span></span>

## <span data-ttu-id="60e10-128">출력</span><span class="sxs-lookup"><span data-stu-id="60e10-128">OUTPUTS</span></span>

### <span data-ttu-id="60e10-129">PSNetworkWatcherConnectionMonitorOutputObject에 대 한.</span><span class="sxs-lookup"><span data-stu-id="60e10-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="60e10-130">상속자</span><span class="sxs-lookup"><span data-stu-id="60e10-130">NOTES</span></span>

## <span data-ttu-id="60e10-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60e10-131">RELATED LINKS</span></span>
