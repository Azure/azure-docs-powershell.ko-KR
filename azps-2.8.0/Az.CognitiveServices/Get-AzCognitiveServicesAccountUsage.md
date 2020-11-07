---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 7d197cdb7ee8fbfa63d8a3b36da5f038a5a0b8de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697540"
---
# <span data-ttu-id="30983-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="30983-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="30983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30983-102">SYNOPSIS</span></span>
<span data-ttu-id="30983-103">인지 서비스 계정에 대 한 현재 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30983-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="30983-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30983-104">SYNTAX</span></span>

### <span data-ttu-id="30983-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="30983-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30983-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30983-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30983-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30983-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30983-108">설명은</span><span class="sxs-lookup"><span data-stu-id="30983-108">DESCRIPTION</span></span>
<span data-ttu-id="30983-109">**AzCognitiveServicesAccountUsage** Cmdlet은 인지 서비스 계정에 대 한 현재 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30983-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="30983-110">예제의</span><span class="sxs-lookup"><span data-stu-id="30983-110">EXAMPLES</span></span>

### <span data-ttu-id="30983-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="30983-111">Example 1</span></span>
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

### <span data-ttu-id="30983-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="30983-112">Example 2</span></span>
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

### <span data-ttu-id="30983-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="30983-113">Example 3</span></span>
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

## <span data-ttu-id="30983-114">변수</span><span class="sxs-lookup"><span data-stu-id="30983-114">PARAMETERS</span></span>

### <span data-ttu-id="30983-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30983-115">-DefaultProfile</span></span>
<span data-ttu-id="30983-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30983-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30983-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30983-117">-InputObject</span></span>
<span data-ttu-id="30983-118">인식 서비스 계정 개체.</span><span class="sxs-lookup"><span data-stu-id="30983-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="30983-119">-이름</span><span class="sxs-lookup"><span data-stu-id="30983-119">-Name</span></span>
<span data-ttu-id="30983-120">인지 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30983-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="30983-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30983-121">-ResourceGroupName</span></span>
<span data-ttu-id="30983-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30983-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="30983-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30983-123">-ResourceId</span></span>
<span data-ttu-id="30983-124">인식 서비스 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="30983-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="30983-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30983-125">CommonParameters</span></span>
<span data-ttu-id="30983-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30983-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30983-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="30983-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30983-128">입력</span><span class="sxs-lookup"><span data-stu-id="30983-128">INPUTS</span></span>

### <span data-ttu-id="30983-129">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="30983-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="30983-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="30983-130">System.String</span></span>

## <span data-ttu-id="30983-131">출력</span><span class="sxs-lookup"><span data-stu-id="30983-131">OUTPUTS</span></span>

### <span data-ttu-id="30983-132">CognitiveServices. PSCognitiveServicesUsage/. \*</span><span class="sxs-lookup"><span data-stu-id="30983-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="30983-133">상속자</span><span class="sxs-lookup"><span data-stu-id="30983-133">NOTES</span></span>

## <span data-ttu-id="30983-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30983-134">RELATED LINKS</span></span>