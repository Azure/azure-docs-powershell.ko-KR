---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: 423834d0dc7a324743795e0d54324a51f1cd04ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012400"
---
# <span data-ttu-id="49dbc-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="49dbc-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="49dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="49dbc-103">확장을 얻을 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-103">The operation to get the extension.</span></span>

## <span data-ttu-id="49dbc-104">구문</span><span class="sxs-lookup"><span data-stu-id="49dbc-104">SYNTAX</span></span>

### <span data-ttu-id="49dbc-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="49dbc-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49dbc-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="49dbc-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="49dbc-107">설명</span><span class="sxs-lookup"><span data-stu-id="49dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="49dbc-108">확장을 얻을 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-108">The operation to get the extension.</span></span>

## <span data-ttu-id="49dbc-109">예제</span><span class="sxs-lookup"><span data-stu-id="49dbc-109">EXAMPLES</span></span>

### <span data-ttu-id="49dbc-110">예제 1: 컴퓨터의 모든 확장 나열</span><span class="sxs-lookup"><span data-stu-id="49dbc-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="49dbc-111">특정 컴퓨터의 모든 확장을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="49dbc-112">예제 2: 머신에서 특정 확장 기능 사용</span><span class="sxs-lookup"><span data-stu-id="49dbc-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="49dbc-113">머신에서 특정 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="49dbc-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49dbc-114">PARAMETERS</span></span>

### <span data-ttu-id="49dbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49dbc-115">-DefaultProfile</span></span>
<span data-ttu-id="49dbc-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dbc-117">-확장</span><span class="sxs-lookup"><span data-stu-id="49dbc-117">-Expand</span></span>
<span data-ttu-id="49dbc-118">작업에 적용할 확장 식입니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dbc-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="49dbc-119">-MachineName</span></span>
<span data-ttu-id="49dbc-120">확장을 포함하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="49dbc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="49dbc-121">-Name</span></span>
<span data-ttu-id="49dbc-122">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-122">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dbc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49dbc-123">-ResourceGroupName</span></span>
<span data-ttu-id="49dbc-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="49dbc-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49dbc-125">-SubscriptionId</span></span>
<span data-ttu-id="49dbc-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="49dbc-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dbc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49dbc-128">CommonParameters</span></span>
<span data-ttu-id="49dbc-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49dbc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49dbc-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49dbc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49dbc-131">입력</span><span class="sxs-lookup"><span data-stu-id="49dbc-131">INPUTS</span></span>

## <span data-ttu-id="49dbc-132">출력</span><span class="sxs-lookup"><span data-stu-id="49dbc-132">OUTPUTS</span></span>

### <span data-ttu-id="49dbc-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="49dbc-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="49dbc-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49dbc-134">NOTES</span></span>

<span data-ttu-id="49dbc-135">별칭</span><span class="sxs-lookup"><span data-stu-id="49dbc-135">ALIASES</span></span>

## <span data-ttu-id="49dbc-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49dbc-136">RELATED LINKS</span></span>

