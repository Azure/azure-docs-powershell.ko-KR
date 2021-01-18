---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 1e2f1daa222714c23f394d362222f9ef1fd1bde4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492687"
---
# <span data-ttu-id="386c5-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="386c5-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="386c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="386c5-102">SYNOPSIS</span></span>
<span data-ttu-id="386c5-103">주어진 구독 또는 리소스 그룹에 대한 Azure Advisor 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="386c5-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="386c5-104">구문</span><span class="sxs-lookup"><span data-stu-id="386c5-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="386c5-105">설명</span><span class="sxs-lookup"><span data-stu-id="386c5-105">DESCRIPTION</span></span>
<span data-ttu-id="386c5-106">구독과 연결된 구성에는 다음 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="386c5-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="386c5-107">구독 수준 구성: 구독에 대해 이 유형의 구성은 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="386c5-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="386c5-108">LowCpuThreshold 및 Exclude는 이 유형의 구성의 유일한 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="386c5-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="386c5-109">ResourceGroup 수준 구성: 구독의 각 ResourceGroup에 대해 하나의 구성만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="386c5-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="386c5-110">제외는 이 유형의 구성의 유일한 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="386c5-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="386c5-111">예제</span><span class="sxs-lookup"><span data-stu-id="386c5-111">EXAMPLES</span></span>

### <span data-ttu-id="386c5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="386c5-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="386c5-113">Azure Advisor 구성 목록을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="386c5-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="386c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="386c5-114">PARAMETERS</span></span>

### <span data-ttu-id="386c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386c5-115">-DefaultProfile</span></span>
<span data-ttu-id="386c5-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="386c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386c5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="386c5-117">-ResourceGroupName</span></span>
<span data-ttu-id="386c5-118">구성의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="386c5-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386c5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386c5-119">CommonParameters</span></span>
<span data-ttu-id="386c5-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="386c5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="386c5-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="386c5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386c5-122">입력</span><span class="sxs-lookup"><span data-stu-id="386c5-122">INPUTS</span></span>

### <span data-ttu-id="386c5-123">없음</span><span class="sxs-lookup"><span data-stu-id="386c5-123">None</span></span>

## <span data-ttu-id="386c5-124">출력</span><span class="sxs-lookup"><span data-stu-id="386c5-124">OUTPUTS</span></span>

### <span data-ttu-id="386c5-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="386c5-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="386c5-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="386c5-126">NOTES</span></span>

## <span data-ttu-id="386c5-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="386c5-127">RELATED LINKS</span></span>
