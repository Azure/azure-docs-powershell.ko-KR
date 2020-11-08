---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211837"
---
# <span data-ttu-id="a1bc8-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1bc8-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="a1bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="a1bc8-103">통합 계정 일괄 처리 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="a1bc8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1bc8-104">SYNTAX</span></span>

### <span data-ttu-id="a1bc8-105">ByIntegrationAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1bc8-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1bc8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1bc8-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1bc8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1bc8-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1bc8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a1bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="a1bc8-109">**Get-AzIntegrationAccountBatchConfiguration** cmdlet은 통합 계정에서 일괄 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="a1bc8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a1bc8-110">EXAMPLES</span></span>

### <span data-ttu-id="a1bc8-111">예제 1: 매개 변수를 기준으로 일괄 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1bc8-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a1bc8-112">"SampleResourceGroup" 리소스 그룹에 포함 된 통합 계정 "sampleIntegrationAccount"에 있는 "sampleBatchConfig" 라는 일괄 처리 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="a1bc8-113">예제 2: 통합 계정의 모든 일괄 처리 구성을 매개 변수를 기준으로 나열</span><span class="sxs-lookup"><span data-stu-id="a1bc8-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a1bc8-114">"SampleResourceGroup" 리소스 그룹에 포함 된 통합 계정 "sampleIntegrationAccount"에 있는 모든 일괄 처리 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="a1bc8-115">변수</span><span class="sxs-lookup"><span data-stu-id="a1bc8-115">PARAMETERS</span></span>

### <span data-ttu-id="a1bc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1bc8-116">-DefaultProfile</span></span>
<span data-ttu-id="a1bc8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1bc8-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a1bc8-118">-Name</span></span>
<span data-ttu-id="a1bc8-119">통합 계정 일괄 처리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1bc8-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="a1bc8-120">-ParentName</span></span>
<span data-ttu-id="a1bc8-121">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-121">The integration account name.</span></span>

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

### <span data-ttu-id="a1bc8-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a1bc8-122">-ParentObject</span></span>
<span data-ttu-id="a1bc8-123">통합 계정 개체</span><span class="sxs-lookup"><span data-stu-id="a1bc8-123">An integration account object.</span></span>

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

### <span data-ttu-id="a1bc8-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a1bc8-124">-ParentResourceId</span></span>
<span data-ttu-id="a1bc8-125">통합 계정 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="a1bc8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1bc8-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1bc8-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-127">The resource group name.</span></span>

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

### <span data-ttu-id="a1bc8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1bc8-128">CommonParameters</span></span>
<span data-ttu-id="a1bc8-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1bc8-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1bc8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1bc8-131">입력</span><span class="sxs-lookup"><span data-stu-id="a1bc8-131">INPUTS</span></span>

### <span data-ttu-id="a1bc8-132">IntegrationAccount를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="a1bc8-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="a1bc8-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a1bc8-133">System.String</span></span>

## <span data-ttu-id="a1bc8-134">출력</span><span class="sxs-lookup"><span data-stu-id="a1bc8-134">OUTPUTS</span></span>

### <span data-ttu-id="a1bc8-135">LogicApp. PSIntegrationAccountBatchConfiguration/.</span><span class="sxs-lookup"><span data-stu-id="a1bc8-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="a1bc8-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a1bc8-136">NOTES</span></span>

## <span data-ttu-id="a1bc8-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1bc8-137">RELATED LINKS</span></span>
