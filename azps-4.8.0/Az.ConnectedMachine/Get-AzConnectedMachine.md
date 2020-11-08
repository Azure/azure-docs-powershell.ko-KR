---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: afb6a5bab6c2761095fb3ab69a2898aeeb53b45c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056723"
---
# <span data-ttu-id="6aaca-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="6aaca-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="6aaca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aaca-102">SYNOPSIS</span></span>
<span data-ttu-id="6aaca-103">하이브리드 컴퓨터의 모델 뷰나 인스턴스 보기에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="6aaca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6aaca-104">SYNTAX</span></span>

### <span data-ttu-id="6aaca-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6aaca-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6aaca-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6aaca-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6aaca-107">목록</span><span class="sxs-lookup"><span data-stu-id="6aaca-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6aaca-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6aaca-108">DESCRIPTION</span></span>
<span data-ttu-id="6aaca-109">하이브리드 컴퓨터의 모델 뷰나 인스턴스 보기에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="6aaca-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6aaca-110">EXAMPLES</span></span>

### <span data-ttu-id="6aaca-111">예제 1: 구독에 연결 된 모든 컴퓨터 나열</span><span class="sxs-lookup"><span data-stu-id="6aaca-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="6aaca-112">구독에 연결 된 모든 컴퓨터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="6aaca-113">구독을 지정 하지 않으면 현재 Azure PowerShell 컨텍스트의 구독이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="6aaca-114">예제 2: 리소스 그룹에 연결 된 모든 컴퓨터 나열</span><span class="sxs-lookup"><span data-stu-id="6aaca-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="6aaca-115">리소스 그룹에 연결 된 모든 컴퓨터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="6aaca-116">예제 3: 리소스 그룹에서 연결 된 컴퓨터를 이름으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="6aaca-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="6aaca-117">리소스 그룹에서 연결 된 컴퓨터를 이름으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="6aaca-118">변수</span><span class="sxs-lookup"><span data-stu-id="6aaca-118">PARAMETERS</span></span>

### <span data-ttu-id="6aaca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aaca-119">-DefaultProfile</span></span>
<span data-ttu-id="6aaca-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aaca-121">-확장</span><span class="sxs-lookup"><span data-stu-id="6aaca-121">-Expand</span></span>
<span data-ttu-id="6aaca-122">작업에 적용할 확장 식입니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aaca-123">-이름</span><span class="sxs-lookup"><span data-stu-id="6aaca-123">-Name</span></span>
<span data-ttu-id="6aaca-124">하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-124">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="6aaca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aaca-125">-ResourceGroupName</span></span>
<span data-ttu-id="6aaca-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aaca-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6aaca-127">-SubscriptionId</span></span>
<span data-ttu-id="6aaca-128">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6aaca-129">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6aaca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aaca-130">CommonParameters</span></span>
<span data-ttu-id="6aaca-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aaca-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6aaca-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aaca-133">입력</span><span class="sxs-lookup"><span data-stu-id="6aaca-133">INPUTS</span></span>

## <span data-ttu-id="6aaca-134">출력</span><span class="sxs-lookup"><span data-stu-id="6aaca-134">OUTPUTS</span></span>

### <span data-ttu-id="6aaca-135">ConnectedMachine. Api20200802를 함께 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6aaca-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="6aaca-136">상속자</span><span class="sxs-lookup"><span data-stu-id="6aaca-136">NOTES</span></span>

<span data-ttu-id="6aaca-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="6aaca-137">ALIASES</span></span>

## <span data-ttu-id="6aaca-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6aaca-138">RELATED LINKS</span></span>

