---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 8201780dd70c758c20660bbb8a97d358049cebf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970539"
---
# <span data-ttu-id="25801-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="25801-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="25801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25801-102">SYNOPSIS</span></span>
<span data-ttu-id="25801-103">공간 앵커 계정 사용</span><span class="sxs-lookup"><span data-stu-id="25801-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="25801-104">구문</span><span class="sxs-lookup"><span data-stu-id="25801-104">SYNTAX</span></span>

### <span data-ttu-id="25801-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="25801-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25801-106">GetParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="25801-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25801-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25801-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25801-108">설명</span><span class="sxs-lookup"><span data-stu-id="25801-108">DESCRIPTION</span></span>
<span data-ttu-id="25801-109">특정 구독 및 리소스 그룹에서 공간 앵커 계정을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="25801-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="25801-110">예제</span><span class="sxs-lookup"><span data-stu-id="25801-110">EXAMPLES</span></span>

### <span data-ttu-id="25801-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="25801-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="25801-112">리소스 그룹 "rg1"에 모든 공간 앵커 계정을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="25801-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="25801-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="25801-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="25801-114">리소스 그룹 "rg1"에서 공간 앵커 계정 "예제"를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="25801-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="25801-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="25801-115">PARAMETERS</span></span>

### <span data-ttu-id="25801-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25801-116">-DefaultProfile</span></span>
<span data-ttu-id="25801-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25801-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25801-118">-Name</span><span class="sxs-lookup"><span data-stu-id="25801-118">-Name</span></span>
<span data-ttu-id="25801-119">공간 앵커 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25801-119">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25801-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25801-120">-ResourceGroupName</span></span>
<span data-ttu-id="25801-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25801-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25801-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25801-122">-ResourceId</span></span>
<span data-ttu-id="25801-123">공간 앵커 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="25801-123">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25801-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25801-124">CommonParameters</span></span>
<span data-ttu-id="25801-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25801-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="25801-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="25801-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25801-127">입력</span><span class="sxs-lookup"><span data-stu-id="25801-127">INPUTS</span></span>

### <span data-ttu-id="25801-128">System.String</span><span class="sxs-lookup"><span data-stu-id="25801-128">System.String</span></span>

## <span data-ttu-id="25801-129">출력</span><span class="sxs-lookup"><span data-stu-id="25801-129">OUTPUTS</span></span>

### <span data-ttu-id="25801-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="25801-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="25801-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25801-131">NOTES</span></span>

## <span data-ttu-id="25801-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25801-132">RELATED LINKS</span></span>
