---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218740"
---
# <span data-ttu-id="97e7c-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="97e7c-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="97e7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="97e7c-103">확장을 가져오는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-103">The operation to get the extension.</span></span>

## <span data-ttu-id="97e7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97e7c-104">SYNTAX</span></span>

### <span data-ttu-id="97e7c-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="97e7c-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97e7c-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="97e7c-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="97e7c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="97e7c-107">DESCRIPTION</span></span>
<span data-ttu-id="97e7c-108">확장을 가져오는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-108">The operation to get the extension.</span></span>

## <span data-ttu-id="97e7c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="97e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="97e7c-110">예제 1: 컴퓨터의 모든 확장 목록</span><span class="sxs-lookup"><span data-stu-id="97e7c-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="97e7c-111">특정 컴퓨터에 대 한 모든 확장명을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="97e7c-112">예제 2: 컴퓨터에서 특정 확장명 가져오기</span><span class="sxs-lookup"><span data-stu-id="97e7c-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="97e7c-113">컴퓨터에서 특정 확장명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="97e7c-114">변수</span><span class="sxs-lookup"><span data-stu-id="97e7c-114">PARAMETERS</span></span>

### <span data-ttu-id="97e7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e7c-115">-DefaultProfile</span></span>
<span data-ttu-id="97e7c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e7c-117">-확장</span><span class="sxs-lookup"><span data-stu-id="97e7c-117">-Expand</span></span>
<span data-ttu-id="97e7c-118">작업에 적용할 확장 식입니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="97e7c-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="97e7c-119">-MachineName</span></span>
<span data-ttu-id="97e7c-120">확장명을 포함 하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="97e7c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="97e7c-121">-Name</span></span>
<span data-ttu-id="97e7c-122">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="97e7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="97e7c-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="97e7c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97e7c-125">-SubscriptionId</span></span>
<span data-ttu-id="97e7c-126">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="97e7c-127">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="97e7c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e7c-128">CommonParameters</span></span>
<span data-ttu-id="97e7c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e7c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e7c-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="97e7c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e7c-131">입력</span><span class="sxs-lookup"><span data-stu-id="97e7c-131">INPUTS</span></span>

## <span data-ttu-id="97e7c-132">출력</span><span class="sxs-lookup"><span data-stu-id="97e7c-132">OUTPUTS</span></span>

### <span data-ttu-id="97e7c-133">ConnectedMachine. Api20200802. i a m.. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="97e7c-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="97e7c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="97e7c-134">NOTES</span></span>

<span data-ttu-id="97e7c-135">별칭과</span><span class="sxs-lookup"><span data-stu-id="97e7c-135">ALIASES</span></span>

## <span data-ttu-id="97e7c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97e7c-136">RELATED LINKS</span></span>

