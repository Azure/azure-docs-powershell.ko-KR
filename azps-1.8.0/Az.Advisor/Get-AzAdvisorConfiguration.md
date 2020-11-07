---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 8829e81afc0549c3d4d29855e6256ab696315f0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689222"
---
# <span data-ttu-id="abf16-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="abf16-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="abf16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf16-102">SYNOPSIS</span></span>
<span data-ttu-id="abf16-103">지정 된 구독 또는 리소스 그룹에 대 한 Azure Advisor 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="abf16-104">구문과</span><span class="sxs-lookup"><span data-stu-id="abf16-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abf16-105">설명은</span><span class="sxs-lookup"><span data-stu-id="abf16-105">DESCRIPTION</span></span>
<span data-ttu-id="abf16-106">구독과 연결 된 구성에는 두 가지 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="abf16-107">구독 수준 구성: 구독에 대해이 유형의 구성은 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="abf16-108">LowCpuThreshold 및 Exclude는이 유형의 구성에 대 한 유일한 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="abf16-109">ResourceGroup 수준 구성: 구독의 각 ResourceGroup에 대 한 구성은 하나만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="abf16-110">Exclude는이 유형의 구성에 대 한 유일한 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="abf16-111">예제의</span><span class="sxs-lookup"><span data-stu-id="abf16-111">EXAMPLES</span></span>

### <span data-ttu-id="abf16-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="abf16-112">Example 1</span></span>
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
<span data-ttu-id="abf16-113">Azure Advisor 구성을 목록으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-113">Retrieves a list of Azure Advisor Configration(s).</span></span>

## <span data-ttu-id="abf16-114">변수</span><span class="sxs-lookup"><span data-stu-id="abf16-114">PARAMETERS</span></span>

### <span data-ttu-id="abf16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf16-115">-DefaultProfile</span></span>
<span data-ttu-id="abf16-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf16-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf16-117">-ResourceGroupName</span></span>
<span data-ttu-id="abf16-118">구성의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="abf16-118">Resource Group name of the configuration</span></span>

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

### <span data-ttu-id="abf16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf16-119">CommonParameters</span></span>
<span data-ttu-id="abf16-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="abf16-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf16-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf16-122">입력</span><span class="sxs-lookup"><span data-stu-id="abf16-122">INPUTS</span></span>

### <span data-ttu-id="abf16-123">않아야</span><span class="sxs-lookup"><span data-stu-id="abf16-123">None</span></span>

## <span data-ttu-id="abf16-124">출력</span><span class="sxs-lookup"><span data-stu-id="abf16-124">OUTPUTS</span></span>

### <span data-ttu-id="abf16-125">PsAzureAdvisorConfigurationData를 통한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="abf16-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="abf16-126">상속자</span><span class="sxs-lookup"><span data-stu-id="abf16-126">NOTES</span></span>

## <span data-ttu-id="abf16-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abf16-127">RELATED LINKS</span></span>
