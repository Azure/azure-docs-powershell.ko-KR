---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2497b41399c79297726bc82e3232934cbd6768d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044519"
---
# <span data-ttu-id="26622-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="26622-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="26622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26622-102">SYNOPSIS</span></span>
<span data-ttu-id="26622-103">공간 앵커 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="26622-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="26622-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26622-104">SYNTAX</span></span>

### <span data-ttu-id="26622-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="26622-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26622-106">GetParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="26622-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26622-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26622-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26622-108">설명은</span><span class="sxs-lookup"><span data-stu-id="26622-108">DESCRIPTION</span></span>
<span data-ttu-id="26622-109">특정 구독 및 리소스 그룹에서 공간 앵커 계정을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="26622-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="26622-110">예제의</span><span class="sxs-lookup"><span data-stu-id="26622-110">EXAMPLES</span></span>

### <span data-ttu-id="26622-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="26622-111">Example 1</span></span>
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

<span data-ttu-id="26622-112">리소스 그룹 "rg1"에 모든 공간 앵커 계정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26622-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="26622-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="26622-113">Example 2</span></span>
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

<span data-ttu-id="26622-114">"Rg1" 리소스 그룹의 공간 앵커 계정 "예"를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26622-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="26622-115">변수</span><span class="sxs-lookup"><span data-stu-id="26622-115">PARAMETERS</span></span>

### <span data-ttu-id="26622-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26622-116">-DefaultProfile</span></span>
<span data-ttu-id="26622-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26622-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26622-118">-이름</span><span class="sxs-lookup"><span data-stu-id="26622-118">-Name</span></span>
<span data-ttu-id="26622-119">공간 앵커 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26622-119">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="26622-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26622-120">-ResourceGroupName</span></span>
<span data-ttu-id="26622-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26622-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="26622-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26622-122">-ResourceId</span></span>
<span data-ttu-id="26622-123">공간 앵커 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="26622-123">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="26622-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26622-124">CommonParameters</span></span>
<span data-ttu-id="26622-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26622-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="26622-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26622-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26622-127">입력</span><span class="sxs-lookup"><span data-stu-id="26622-127">INPUTS</span></span>

### <span data-ttu-id="26622-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26622-128">System.String</span></span>

## <span data-ttu-id="26622-129">출력</span><span class="sxs-lookup"><span data-stu-id="26622-129">OUTPUTS</span></span>

### <span data-ttu-id="26622-130">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="26622-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="26622-131">상속자</span><span class="sxs-lookup"><span data-stu-id="26622-131">NOTES</span></span>

## <span data-ttu-id="26622-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26622-132">RELATED LINKS</span></span>
