---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047977"
---
# <span data-ttu-id="410c7-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="410c7-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="410c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="410c7-102">SYNOPSIS</span></span>
<span data-ttu-id="410c7-103">Application insights 연결 된 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="410c7-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="410c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="410c7-104">SYNTAX</span></span>

### <span data-ttu-id="410c7-105">ByResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="410c7-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="410c7-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="410c7-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="410c7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="410c7-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="410c7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="410c7-108">DESCRIPTION</span></span>
<span data-ttu-id="410c7-109">Application insights 연결 된 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="410c7-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="410c7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="410c7-110">EXAMPLES</span></span>

### <span data-ttu-id="410c7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="410c7-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="410c7-112">"ComponentName" 구성 요소와 연결 된 연결 된 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="410c7-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="410c7-113">변수</span><span class="sxs-lookup"><span data-stu-id="410c7-113">PARAMETERS</span></span>

### <span data-ttu-id="410c7-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="410c7-114">-ComponentName</span></span>
<span data-ttu-id="410c7-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="410c7-115">Component Name</span></span>

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

### <span data-ttu-id="410c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410c7-116">-DefaultProfile</span></span>
<span data-ttu-id="410c7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="410c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="410c7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="410c7-118">-InputObject</span></span>
<span data-ttu-id="410c7-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="410c7-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="410c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="410c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="410c7-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="410c7-121">Resource Group Name</span></span>

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

### <span data-ttu-id="410c7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="410c7-122">-ResourceId</span></span>
<span data-ttu-id="410c7-123">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="410c7-123">Component ResourceId</span></span>

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

### <span data-ttu-id="410c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410c7-124">CommonParameters</span></span>
<span data-ttu-id="410c7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="410c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410c7-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="410c7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410c7-127">입력</span><span class="sxs-lookup"><span data-stu-id="410c7-127">INPUTS</span></span>

### <span data-ttu-id="410c7-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="410c7-128">System.String</span></span>

### <span data-ttu-id="410c7-129">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="410c7-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="410c7-130">출력</span><span class="sxs-lookup"><span data-stu-id="410c7-130">OUTPUTS</span></span>

### <span data-ttu-id="410c7-131">PSComponentLinkedStorageAccounts-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="410c7-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="410c7-132">상속자</span><span class="sxs-lookup"><span data-stu-id="410c7-132">NOTES</span></span>

## <span data-ttu-id="410c7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="410c7-133">RELATED LINKS</span></span>
