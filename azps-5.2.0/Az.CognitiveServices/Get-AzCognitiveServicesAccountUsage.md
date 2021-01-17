---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: c287fd6aafcfe63a26c5f1dfd01503adb741428d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338721"
---
# <span data-ttu-id="40d08-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="40d08-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="40d08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40d08-102">SYNOPSIS</span></span>
<span data-ttu-id="40d08-103">Cognitive Services 계정에 대한 현재 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40d08-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="40d08-104">구문</span><span class="sxs-lookup"><span data-stu-id="40d08-104">SYNTAX</span></span>

### <span data-ttu-id="40d08-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="40d08-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40d08-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d08-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40d08-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d08-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40d08-108">설명</span><span class="sxs-lookup"><span data-stu-id="40d08-108">DESCRIPTION</span></span>
<span data-ttu-id="40d08-109">**Get-AzCognitiveServicesAccountUsage** cmdlet은 Cognitive Services 계정에 대한 현재 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40d08-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="40d08-110">예제</span><span class="sxs-lookup"><span data-stu-id="40d08-110">EXAMPLES</span></span>

### <span data-ttu-id="40d08-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="40d08-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="40d08-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="40d08-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="40d08-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="40d08-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="40d08-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40d08-114">PARAMETERS</span></span>

### <span data-ttu-id="40d08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d08-115">-DefaultProfile</span></span>
<span data-ttu-id="40d08-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40d08-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d08-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40d08-117">-InputObject</span></span>
<span data-ttu-id="40d08-118">Cognitive Services 계정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="40d08-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40d08-119">-Name</span><span class="sxs-lookup"><span data-stu-id="40d08-119">-Name</span></span>
<span data-ttu-id="40d08-120">Cognitive Services 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40d08-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d08-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d08-121">-ResourceGroupName</span></span>
<span data-ttu-id="40d08-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40d08-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d08-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40d08-123">-ResourceId</span></span>
<span data-ttu-id="40d08-124">Cognitive Services 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="40d08-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d08-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d08-125">CommonParameters</span></span>
<span data-ttu-id="40d08-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40d08-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d08-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40d08-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d08-128">입력</span><span class="sxs-lookup"><span data-stu-id="40d08-128">INPUTS</span></span>

### <span data-ttu-id="40d08-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="40d08-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="40d08-130">System.String</span><span class="sxs-lookup"><span data-stu-id="40d08-130">System.String</span></span>

## <span data-ttu-id="40d08-131">출력</span><span class="sxs-lookup"><span data-stu-id="40d08-131">OUTPUTS</span></span>

### <span data-ttu-id="40d08-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="40d08-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="40d08-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40d08-133">NOTES</span></span>

## <span data-ttu-id="40d08-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40d08-134">RELATED LINKS</span></span>
