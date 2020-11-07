---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: e6f4562daf77204a96991ddeef9164f2f6aff17a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696732"
---
# <span data-ttu-id="8da02-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="8da02-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="8da02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da02-102">SYNOPSIS</span></span>
<span data-ttu-id="8da02-103">공유 구독의 원본 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8da02-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="8da02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8da02-104">SYNTAX</span></span>

### <span data-ttu-id="8da02-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8da02-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8da02-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da02-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8da02-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8da02-107">DESCRIPTION</span></span>
<span data-ttu-id="8da02-108">**AzDataShareSourceDataSet** cmdlet은 공유 구독의 원본 데이터 집합에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da02-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="8da02-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8da02-109">EXAMPLES</span></span>

### <span data-ttu-id="8da02-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8da02-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="8da02-111">원본 공유에서 사용할 수 있는 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8da02-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="8da02-112">변수</span><span class="sxs-lookup"><span data-stu-id="8da02-112">PARAMETERS</span></span>

### <span data-ttu-id="8da02-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8da02-113">-AccountName</span></span>
<span data-ttu-id="8da02-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="8da02-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da02-115">-DefaultProfile</span></span>
<span data-ttu-id="8da02-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8da02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8da02-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da02-117">-ResourceGroupName</span></span>
<span data-ttu-id="8da02-118">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8da02-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da02-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8da02-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="8da02-120">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="8da02-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da02-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="8da02-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="8da02-122">Azure data share 구독 리소스 id</span><span class="sxs-lookup"><span data-stu-id="8da02-122">Azure data share subscription resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da02-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da02-123">CommonParameters</span></span>
<span data-ttu-id="8da02-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da02-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da02-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da02-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da02-126">입력</span><span class="sxs-lookup"><span data-stu-id="8da02-126">INPUTS</span></span>

### <span data-ttu-id="8da02-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8da02-127">System.String</span></span>

## <span data-ttu-id="8da02-128">출력</span><span class="sxs-lookup"><span data-stu-id="8da02-128">OUTPUTS</span></span>

### <span data-ttu-id="8da02-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="8da02-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="8da02-130">상속자</span><span class="sxs-lookup"><span data-stu-id="8da02-130">NOTES</span></span>

## <span data-ttu-id="8da02-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8da02-131">RELATED LINKS</span></span>