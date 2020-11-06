---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: 1cdfaa6b57a0bcf6d50e0e3a77f80c1a5c069069
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526256"
---
# <span data-ttu-id="65e1b-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="65e1b-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="65e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="65e1b-103">인지 서비스 계정에 대 한 현재 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65e1b-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65e1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65e1b-104">SYNTAX</span></span>

### <span data-ttu-id="65e1b-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="65e1b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65e1b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65e1b-106">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65e1b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65e1b-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65e1b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="65e1b-108">DESCRIPTION</span></span>
<span data-ttu-id="65e1b-109">**AzureRmCognitiveServicesAccountUsage** Cmdlet은 인지 서비스 계정에 대 한 현재 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65e1b-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="65e1b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="65e1b-110">EXAMPLES</span></span>

### <span data-ttu-id="65e1b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="65e1b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="65e1b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="65e1b-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="65e1b-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="65e1b-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="65e1b-114">변수</span><span class="sxs-lookup"><span data-stu-id="65e1b-114">PARAMETERS</span></span>

### <span data-ttu-id="65e1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e1b-115">-DefaultProfile</span></span>
<span data-ttu-id="65e1b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65e1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e1b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65e1b-117">-InputObject</span></span>
<span data-ttu-id="65e1b-118">인식 서비스 계정 개체.</span><span class="sxs-lookup"><span data-stu-id="65e1b-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="65e1b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="65e1b-119">-Name</span></span>
<span data-ttu-id="65e1b-120">인지 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65e1b-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="65e1b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e1b-121">-ResourceGroupName</span></span>
<span data-ttu-id="65e1b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65e1b-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="65e1b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65e1b-123">-ResourceId</span></span>
<span data-ttu-id="65e1b-124">인식 서비스 계정 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="65e1b-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="65e1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e1b-125">CommonParameters</span></span>
<span data-ttu-id="65e1b-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e1b-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e1b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e1b-128">입력</span><span class="sxs-lookup"><span data-stu-id="65e1b-128">INPUTS</span></span>

### <span data-ttu-id="65e1b-129">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="65e1b-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>
<span data-ttu-id="65e1b-130">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65e1b-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="65e1b-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="65e1b-131">System.String</span></span>

## <span data-ttu-id="65e1b-132">출력</span><span class="sxs-lookup"><span data-stu-id="65e1b-132">OUTPUTS</span></span>

### <span data-ttu-id="65e1b-133">CognitiveServices. PSCognitiveServicesUsage/. \*</span><span class="sxs-lookup"><span data-stu-id="65e1b-133">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="65e1b-134">상속자</span><span class="sxs-lookup"><span data-stu-id="65e1b-134">NOTES</span></span>

## <span data-ttu-id="65e1b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65e1b-135">RELATED LINKS</span></span>
