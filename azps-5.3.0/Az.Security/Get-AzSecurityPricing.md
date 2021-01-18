---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495000"
---
# <span data-ttu-id="4bf16-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="4bf16-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="4bf16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bf16-102">SYNOPSIS</span></span>

<span data-ttu-id="4bf16-103">Azure Security Center에서 구독에 대한 Azure Defender 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bf16-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="4bf16-104">구문</span><span class="sxs-lookup"><span data-stu-id="4bf16-104">SYNTAX</span></span>

### <span data-ttu-id="4bf16-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="4bf16-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bf16-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4bf16-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bf16-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bf16-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bf16-108">설명</span><span class="sxs-lookup"><span data-stu-id="4bf16-108">DESCRIPTION</span></span>

<span data-ttu-id="4bf16-109">이 cmdlet을 사용하여 구독당 각 Azure Defender 계획을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bf16-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="4bf16-110">Azure Defender 및 사용 가능한 계획에 대한 자세한 내용은 [Azure Defender 소개를 참조하세요.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="4bf16-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="4bf16-111">예제</span><span class="sxs-lookup"><span data-stu-id="4bf16-111">EXAMPLES</span></span>

### <span data-ttu-id="4bf16-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bf16-112">Example 1</span></span>

```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                   Name                      PricingTier    FreeTrialRemainingTime
--                                                                                                                   ----                      -----------    ----------------------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines            VirtualMachines           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/Sqlservers                 SqlServers                Standard       00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices                AppServices               Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts            StorageAccounts           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlserverVirtualMachines   SqlservervirtualMachines  Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService          KubernetesService         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry          ContainerRegistry         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults                  KeyVaults                 Free           00:00:00
```

<span data-ttu-id="4bf16-113">구독에 대한 각 Azure Defender 계획의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bf16-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="4bf16-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="4bf16-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="4bf16-115">특정 리소스 ID의 가격 책정 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bf16-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="4bf16-116">여기서 ResourceId는 . `Get-AzSecurityPricing`</span><span class="sxs-lookup"><span data-stu-id="4bf16-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="4bf16-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="4bf16-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="4bf16-118">명명된 Azure Defender 계획의 가격 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bf16-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="4bf16-119">여기서 `name` 반환되는 이름 중 하나입니다. `Get-AzSecurityPricing`</span><span class="sxs-lookup"><span data-stu-id="4bf16-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="4bf16-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bf16-120">PARAMETERS</span></span>

### <span data-ttu-id="4bf16-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf16-121">-DefaultProfile</span></span>

<span data-ttu-id="4bf16-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bf16-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bf16-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4bf16-123">-Name</span></span>

<span data-ttu-id="4bf16-124">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bf16-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf16-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bf16-125">-ResourceId</span></span>

<span data-ttu-id="4bf16-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bf16-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf16-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf16-127">CommonParameters</span></span>

<span data-ttu-id="4bf16-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4bf16-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf16-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4bf16-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf16-130">입력</span><span class="sxs-lookup"><span data-stu-id="4bf16-130">INPUTS</span></span>

### <span data-ttu-id="4bf16-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4bf16-131">System.String</span></span>

## <span data-ttu-id="4bf16-132">출력</span><span class="sxs-lookup"><span data-stu-id="4bf16-132">OUTPUTS</span></span>

### <span data-ttu-id="4bf16-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="4bf16-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="4bf16-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4bf16-134">NOTES</span></span>

## <span data-ttu-id="4bf16-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bf16-135">RELATED LINKS</span></span>
