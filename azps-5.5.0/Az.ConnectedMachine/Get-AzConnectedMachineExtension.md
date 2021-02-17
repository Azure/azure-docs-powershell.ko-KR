---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209920"
---
# <span data-ttu-id="bb2f8-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="bb2f8-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="bb2f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb2f8-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2f8-103">확장을 얻을 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-103">The operation to get the extension.</span></span>

## <span data-ttu-id="bb2f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="bb2f8-104">SYNTAX</span></span>

### <span data-ttu-id="bb2f8-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="bb2f8-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bb2f8-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="bb2f8-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bb2f8-107">설명</span><span class="sxs-lookup"><span data-stu-id="bb2f8-107">DESCRIPTION</span></span>
<span data-ttu-id="bb2f8-108">확장을 얻을 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-108">The operation to get the extension.</span></span>

## <span data-ttu-id="bb2f8-109">예제</span><span class="sxs-lookup"><span data-stu-id="bb2f8-109">EXAMPLES</span></span>

### <span data-ttu-id="bb2f8-110">예제 1: 컴퓨터의 모든 확장 나열</span><span class="sxs-lookup"><span data-stu-id="bb2f8-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="bb2f8-111">특정 머신에 대한 모든 확장을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="bb2f8-112">예제 2: 머신에서 특정 확장하기</span><span class="sxs-lookup"><span data-stu-id="bb2f8-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="bb2f8-113">머신에서 특정 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="bb2f8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb2f8-114">PARAMETERS</span></span>

### <span data-ttu-id="bb2f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb2f8-115">-DefaultProfile</span></span>
<span data-ttu-id="bb2f8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb2f8-117">-Expand</span><span class="sxs-lookup"><span data-stu-id="bb2f8-117">-Expand</span></span>
<span data-ttu-id="bb2f8-118">작업에 적용할 확장 식입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="bb2f8-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="bb2f8-119">-MachineName</span></span>
<span data-ttu-id="bb2f8-120">확장을 포함하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="bb2f8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bb2f8-121">-Name</span></span>
<span data-ttu-id="bb2f8-122">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="bb2f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb2f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb2f8-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb2f8-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb2f8-125">-SubscriptionId</span></span>
<span data-ttu-id="bb2f8-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bb2f8-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bb2f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2f8-128">CommonParameters</span></span>
<span data-ttu-id="bb2f8-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2f8-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb2f8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2f8-131">입력</span><span class="sxs-lookup"><span data-stu-id="bb2f8-131">INPUTS</span></span>

## <span data-ttu-id="bb2f8-132">출력</span><span class="sxs-lookup"><span data-stu-id="bb2f8-132">OUTPUTS</span></span>

### <span data-ttu-id="bb2f8-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="bb2f8-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="bb2f8-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bb2f8-134">NOTES</span></span>

<span data-ttu-id="bb2f8-135">별칭</span><span class="sxs-lookup"><span data-stu-id="bb2f8-135">ALIASES</span></span>

## <span data-ttu-id="bb2f8-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb2f8-136">RELATED LINKS</span></span>

