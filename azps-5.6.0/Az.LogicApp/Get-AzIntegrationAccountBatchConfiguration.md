---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 722f2bd79230de11c12ab0448fb39ed3ad49f00d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960704"
---
# <span data-ttu-id="f42ea-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f42ea-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="f42ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f42ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f42ea-103">통합 계정 일괄 처리 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="f42ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="f42ea-104">SYNTAX</span></span>

### <span data-ttu-id="f42ea-105">ByIntegrationAccount(기본값)</span><span class="sxs-lookup"><span data-stu-id="f42ea-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f42ea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f42ea-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f42ea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f42ea-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f42ea-108">설명</span><span class="sxs-lookup"><span data-stu-id="f42ea-108">DESCRIPTION</span></span>
<span data-ttu-id="f42ea-109">**Get-AzIntegrationAccountBatchConfiguration** cmdlet은 통합 계정에서 일괄 처리 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="f42ea-110">예제</span><span class="sxs-lookup"><span data-stu-id="f42ea-110">EXAMPLES</span></span>

### <span data-ttu-id="f42ea-111">예제 1: 매개 변수에 따라 일괄 처리 구성을 얻다</span><span class="sxs-lookup"><span data-stu-id="f42ea-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="f42ea-112">"sampleResourceGroup"에 포함된 통합 계정 "sampleIntegrationAccount"에 있는 "sampleBatchConfig"라는 일괄 처리 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="f42ea-113">예제 2: 매개 변수에 따라 통합 계정에 모든 일괄 처리 구성 나열</span><span class="sxs-lookup"><span data-stu-id="f42ea-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="f42ea-114">"sampleResourceGroup"에 포함된 통합 계정 "sampleIntegrationAccount"에 있는 모든 일괄 처리 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="f42ea-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f42ea-115">PARAMETERS</span></span>

### <span data-ttu-id="f42ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f42ea-116">-DefaultProfile</span></span>
<span data-ttu-id="f42ea-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f42ea-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f42ea-118">-Name</span></span>
<span data-ttu-id="f42ea-119">통합 계정 일괄 처리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="f42ea-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="f42ea-120">-ParentName</span></span>
<span data-ttu-id="f42ea-121">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-121">The integration account name.</span></span>

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

### <span data-ttu-id="f42ea-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f42ea-122">-ParentObject</span></span>
<span data-ttu-id="f42ea-123">통합 계정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-123">An integration account object.</span></span>

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

### <span data-ttu-id="f42ea-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f42ea-124">-ParentResourceId</span></span>
<span data-ttu-id="f42ea-125">통합 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="f42ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f42ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="f42ea-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-127">The resource group name.</span></span>

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

### <span data-ttu-id="f42ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f42ea-128">CommonParameters</span></span>
<span data-ttu-id="f42ea-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f42ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f42ea-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f42ea-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f42ea-131">입력</span><span class="sxs-lookup"><span data-stu-id="f42ea-131">INPUTS</span></span>

### <span data-ttu-id="f42ea-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="f42ea-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="f42ea-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f42ea-133">System.String</span></span>

## <span data-ttu-id="f42ea-134">출력</span><span class="sxs-lookup"><span data-stu-id="f42ea-134">OUTPUTS</span></span>

### <span data-ttu-id="f42ea-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f42ea-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="f42ea-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f42ea-136">NOTES</span></span>

## <span data-ttu-id="f42ea-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f42ea-137">RELATED LINKS</span></span>
