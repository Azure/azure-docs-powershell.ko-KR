---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: f739c5fa018a4d4f4ebf553c76dbacd35ee315c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189044"
---
# <span data-ttu-id="dd9e6-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="dd9e6-101">Get-AzSignalR</span></span>

## <span data-ttu-id="dd9e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9e6-103">리소스 그룹 또는 구독에서 특정 SignalR 서비스 또는 모든 SignalR 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="dd9e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="dd9e6-104">SYNTAX</span></span>

### <span data-ttu-id="dd9e6-105">ListSignalRServiceParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dd9e6-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd9e6-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd9e6-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd9e6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd9e6-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd9e6-108">설명</span><span class="sxs-lookup"><span data-stu-id="dd9e6-108">DESCRIPTION</span></span>
<span data-ttu-id="dd9e6-109">리소스 그룹 또는 구독에서 특정 SignalR 서비스 또는 모든 SignalR 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="dd9e6-110">예제</span><span class="sxs-lookup"><span data-stu-id="dd9e6-110">EXAMPLES</span></span>

### <span data-ttu-id="dd9e6-111">구독의 모든 SignalR Services를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="dd9e6-112">리소스 그룹의 모든 SignalR Services를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="dd9e6-113">특정 SignalR Service를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="dd9e6-114">기본 리소스 그룹에서 특정 SignalR Service를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="dd9e6-115">기본 리소스 그룹은 \` Set-AzDefault -ResourceGroupName myResourceGroup으로 설정할 수 \` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="dd9e6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd9e6-116">PARAMETERS</span></span>

### <span data-ttu-id="dd9e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9e6-117">-DefaultProfile</span></span>
<span data-ttu-id="dd9e6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd9e6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dd9e6-119">-Name</span></span>
<span data-ttu-id="dd9e6-120">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-120">SignalR service name.</span></span>

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

### <span data-ttu-id="dd9e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd9e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd9e6-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd9e6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd9e6-123">-ResourceId</span></span>
<span data-ttu-id="dd9e6-124">SignalR Service 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="dd9e6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9e6-125">CommonParameters</span></span>
<span data-ttu-id="dd9e6-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9e6-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dd9e6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9e6-128">입력</span><span class="sxs-lookup"><span data-stu-id="dd9e6-128">INPUTS</span></span>

### <span data-ttu-id="dd9e6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dd9e6-129">System.String</span></span>
## <span data-ttu-id="dd9e6-130">출력</span><span class="sxs-lookup"><span data-stu-id="dd9e6-130">OUTPUTS</span></span>

### <span data-ttu-id="dd9e6-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="dd9e6-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="dd9e6-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dd9e6-132">NOTES</span></span>

## <span data-ttu-id="dd9e6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd9e6-133">RELATED LINKS</span></span>
