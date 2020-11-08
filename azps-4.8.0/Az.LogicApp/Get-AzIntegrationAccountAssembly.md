---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211841"
---
# <span data-ttu-id="16d05-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="16d05-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="16d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d05-102">SYNOPSIS</span></span>
<span data-ttu-id="16d05-103">통합 계정 어셈블리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="16d05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16d05-104">SYNTAX</span></span>

### <span data-ttu-id="16d05-105">ByIntegrationAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="16d05-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d05-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="16d05-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d05-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16d05-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16d05-108">설명은</span><span class="sxs-lookup"><span data-stu-id="16d05-108">DESCRIPTION</span></span>
<span data-ttu-id="16d05-109">**Get-AzIntegrationAccountAssembly** cmdlet은 통합 계정에서 어셈블리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="16d05-110">예제의</span><span class="sxs-lookup"><span data-stu-id="16d05-110">EXAMPLES</span></span>

### <span data-ttu-id="16d05-111">예제 1: 매개 변수를 기준으로 어셈블리 가져오기</span><span class="sxs-lookup"><span data-stu-id="16d05-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="16d05-112">"SampleResourceGroup" 리소스 그룹에 포함 된 통합 계정 "sampleIntegrationAccount"에 있는 "sampleAssembly" 라는 어셈블리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="16d05-113">예제 2: 통합 계정의 모든 어셈블리를 매개 변수로 나열</span><span class="sxs-lookup"><span data-stu-id="16d05-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="16d05-114">리소스 그룹 "sampleResourceGroup"에 포함 되어 있는 통합 계정 "sampleIntegrationAccount"에 있는 모든 어셈블리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="16d05-115">변수</span><span class="sxs-lookup"><span data-stu-id="16d05-115">PARAMETERS</span></span>

### <span data-ttu-id="16d05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d05-116">-DefaultProfile</span></span>
<span data-ttu-id="16d05-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16d05-118">-이름</span><span class="sxs-lookup"><span data-stu-id="16d05-118">-Name</span></span>
<span data-ttu-id="16d05-119">통합 계정 어셈블리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d05-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="16d05-120">-ParentName</span></span>
<span data-ttu-id="16d05-121">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d05-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="16d05-122">-ParentObject</span></span>
<span data-ttu-id="16d05-123">통합 계정 개체</span><span class="sxs-lookup"><span data-stu-id="16d05-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16d05-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="16d05-124">-ParentResourceId</span></span>
<span data-ttu-id="16d05-125">통합 계정 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d05-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d05-126">-ResourceGroupName</span></span>
<span data-ttu-id="16d05-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d05-128">CommonParameters</span></span>
<span data-ttu-id="16d05-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d05-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d05-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d05-131">입력</span><span class="sxs-lookup"><span data-stu-id="16d05-131">INPUTS</span></span>

### <span data-ttu-id="16d05-132">IntegrationAccount를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="16d05-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="16d05-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16d05-133">System.String</span></span>

## <span data-ttu-id="16d05-134">출력</span><span class="sxs-lookup"><span data-stu-id="16d05-134">OUTPUTS</span></span>

### <span data-ttu-id="16d05-135">LogicApp. PSIntegrationAccountAssembly/.</span><span class="sxs-lookup"><span data-stu-id="16d05-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="16d05-136">상속자</span><span class="sxs-lookup"><span data-stu-id="16d05-136">NOTES</span></span>

## <span data-ttu-id="16d05-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16d05-137">RELATED LINKS</span></span>
