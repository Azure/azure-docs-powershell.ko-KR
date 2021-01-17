---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353546"
---
# <span data-ttu-id="68db3-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68db3-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="68db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68db3-102">SYNOPSIS</span></span>
<span data-ttu-id="68db3-103">Application Insights 연결된 저장소 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="68db3-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="68db3-104">구문</span><span class="sxs-lookup"><span data-stu-id="68db3-104">SYNTAX</span></span>

### <span data-ttu-id="68db3-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="68db3-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68db3-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68db3-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68db3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68db3-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68db3-108">설명</span><span class="sxs-lookup"><span data-stu-id="68db3-108">DESCRIPTION</span></span>
<span data-ttu-id="68db3-109">Application Insights 연결된 저장소 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="68db3-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="68db3-110">예제</span><span class="sxs-lookup"><span data-stu-id="68db3-110">EXAMPLES</span></span>

### <span data-ttu-id="68db3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="68db3-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="68db3-112">구성 요소 "componentName"에 연결된 저장소 계정을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68db3-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="68db3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68db3-113">PARAMETERS</span></span>

### <span data-ttu-id="68db3-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="68db3-114">-ComponentName</span></span>
<span data-ttu-id="68db3-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="68db3-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68db3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68db3-116">-DefaultProfile</span></span>
<span data-ttu-id="68db3-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68db3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68db3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68db3-118">-InputObject</span></span>
<span data-ttu-id="68db3-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="68db3-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68db3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68db3-120">-ResourceGroupName</span></span>
<span data-ttu-id="68db3-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="68db3-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68db3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68db3-122">-ResourceId</span></span>
<span data-ttu-id="68db3-123">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="68db3-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68db3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68db3-124">CommonParameters</span></span>
<span data-ttu-id="68db3-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68db3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68db3-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68db3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68db3-127">입력</span><span class="sxs-lookup"><span data-stu-id="68db3-127">INPUTS</span></span>

### <span data-ttu-id="68db3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="68db3-128">System.String</span></span>

### <span data-ttu-id="68db3-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="68db3-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="68db3-130">출력</span><span class="sxs-lookup"><span data-stu-id="68db3-130">OUTPUTS</span></span>

### <span data-ttu-id="68db3-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="68db3-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="68db3-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68db3-132">NOTES</span></span>

## <span data-ttu-id="68db3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68db3-133">RELATED LINKS</span></span>
