---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 588f9a057767e1e78b43664c35a61f26e6edf972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016000"
---
# <span data-ttu-id="edac6-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="edac6-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="edac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edac6-102">SYNOPSIS</span></span>

<span data-ttu-id="edac6-103">Azure Security Center에서 구독에 대한 Azure Defender 요금제가 도착합니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="edac6-104">구문</span><span class="sxs-lookup"><span data-stu-id="edac6-104">SYNTAX</span></span>

### <span data-ttu-id="edac6-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="edac6-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edac6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="edac6-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edac6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="edac6-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edac6-108">설명</span><span class="sxs-lookup"><span data-stu-id="edac6-108">DESCRIPTION</span></span>

<span data-ttu-id="edac6-109">이 cmdlet을 사용하여 구독당 각 Azure Defender 계획을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="edac6-110">Azure Defender 및 사용 가능한 계획에 대한 자세한 내용은 Azure Defender 소개 [를 참조하세요.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="edac6-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="edac6-111">예제</span><span class="sxs-lookup"><span data-stu-id="edac6-111">EXAMPLES</span></span>

### <span data-ttu-id="edac6-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="edac6-112">Example 1</span></span>

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

<span data-ttu-id="edac6-113">구독에 대한 각 Azure Defender 계획의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="edac6-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="edac6-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="edac6-115">특정 리소스 ID의 가격 책정 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="edac6-116">ResourceId가 에 의해 반환된 신분의 하나인 경우 `Get-AzSecurityPricing`</span><span class="sxs-lookup"><span data-stu-id="edac6-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="edac6-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="edac6-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="edac6-118">명명된 Azure Defender 계획의 가격 책정 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="edac6-119">에서 `name` 반환되는 이름 중 하나는 어디에 `Get-AzSecurityPricing` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="edac6-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="edac6-120">PARAMETERS</span></span>

### <span data-ttu-id="edac6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edac6-121">-DefaultProfile</span></span>

<span data-ttu-id="edac6-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edac6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="edac6-123">-Name</span></span>

<span data-ttu-id="edac6-124">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-124">Resource name.</span></span>

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

### <span data-ttu-id="edac6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edac6-125">-ResourceId</span></span>

<span data-ttu-id="edac6-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-126">Resource ID.</span></span>

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

### <span data-ttu-id="edac6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edac6-127">CommonParameters</span></span>

<span data-ttu-id="edac6-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="edac6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edac6-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="edac6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edac6-130">입력</span><span class="sxs-lookup"><span data-stu-id="edac6-130">INPUTS</span></span>

### <span data-ttu-id="edac6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="edac6-131">System.String</span></span>

## <span data-ttu-id="edac6-132">출력</span><span class="sxs-lookup"><span data-stu-id="edac6-132">OUTPUTS</span></span>

### <span data-ttu-id="edac6-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="edac6-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="edac6-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="edac6-134">NOTES</span></span>

## <span data-ttu-id="edac6-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edac6-135">RELATED LINKS</span></span>
