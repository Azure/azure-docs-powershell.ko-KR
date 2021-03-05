---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: a059209e993f17ffb5eed1b29d1854f8387f3d8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965232"
---
# <span data-ttu-id="574fd-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="574fd-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="574fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="574fd-102">SYNOPSIS</span></span>
<span data-ttu-id="574fd-103">애플리케이션 인사이트 연결된 저장소 계정 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="574fd-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="574fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="574fd-104">SYNTAX</span></span>

### <span data-ttu-id="574fd-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="574fd-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="574fd-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="574fd-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="574fd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="574fd-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="574fd-108">설명</span><span class="sxs-lookup"><span data-stu-id="574fd-108">DESCRIPTION</span></span>
<span data-ttu-id="574fd-109">애플리케이션 인사이트 연결된 저장소 계정 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="574fd-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="574fd-110">예제</span><span class="sxs-lookup"><span data-stu-id="574fd-110">EXAMPLES</span></span>

### <span data-ttu-id="574fd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="574fd-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="574fd-112">구성 요소 "componentName"와 연결된 연결된 저장소 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="574fd-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="574fd-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="574fd-113">PARAMETERS</span></span>

### <span data-ttu-id="574fd-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="574fd-114">-ComponentName</span></span>
<span data-ttu-id="574fd-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="574fd-115">Component Name</span></span>

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

### <span data-ttu-id="574fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574fd-116">-DefaultProfile</span></span>
<span data-ttu-id="574fd-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="574fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="574fd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="574fd-118">-InputObject</span></span>
<span data-ttu-id="574fd-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="574fd-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="574fd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="574fd-120">-ResourceGroupName</span></span>
<span data-ttu-id="574fd-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="574fd-121">Resource Group Name</span></span>

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

### <span data-ttu-id="574fd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="574fd-122">-ResourceId</span></span>
<span data-ttu-id="574fd-123">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="574fd-123">Component ResourceId</span></span>

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

### <span data-ttu-id="574fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574fd-124">CommonParameters</span></span>
<span data-ttu-id="574fd-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="574fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574fd-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="574fd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574fd-127">입력</span><span class="sxs-lookup"><span data-stu-id="574fd-127">INPUTS</span></span>

### <span data-ttu-id="574fd-128">System.String</span><span class="sxs-lookup"><span data-stu-id="574fd-128">System.String</span></span>

### <span data-ttu-id="574fd-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="574fd-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="574fd-130">출력</span><span class="sxs-lookup"><span data-stu-id="574fd-130">OUTPUTS</span></span>

### <span data-ttu-id="574fd-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="574fd-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="574fd-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="574fd-132">NOTES</span></span>

## <span data-ttu-id="574fd-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="574fd-133">RELATED LINKS</span></span>
