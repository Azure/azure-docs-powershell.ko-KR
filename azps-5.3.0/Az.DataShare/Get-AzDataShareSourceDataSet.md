---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377399"
---
# <span data-ttu-id="4cb6f-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="4cb6f-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="4cb6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb6f-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb6f-103">공유 구독의 원본 데이터 집합에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="4cb6f-104">구문</span><span class="sxs-lookup"><span data-stu-id="4cb6f-104">SYNTAX</span></span>

### <span data-ttu-id="4cb6f-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4cb6f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cb6f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cb6f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cb6f-107">설명</span><span class="sxs-lookup"><span data-stu-id="4cb6f-107">DESCRIPTION</span></span>
<span data-ttu-id="4cb6f-108">**Get-AzDataShareSourceDataSet** cmdlet은 공유 구독의 원본 데이터 집합에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="4cb6f-109">예제</span><span class="sxs-lookup"><span data-stu-id="4cb6f-109">EXAMPLES</span></span>

### <span data-ttu-id="4cb6f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4cb6f-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="4cb6f-111">원본 공유에서 사용할 수 있는 데이터 세트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="4cb6f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cb6f-112">PARAMETERS</span></span>

### <span data-ttu-id="4cb6f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4cb6f-113">-AccountName</span></span>
<span data-ttu-id="4cb6f-114">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="4cb6f-114">Azure data share account name</span></span>

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

### <span data-ttu-id="4cb6f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb6f-115">-DefaultProfile</span></span>
<span data-ttu-id="4cb6f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cb6f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb6f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4cb6f-118">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4cb6f-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4cb6f-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4cb6f-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="4cb6f-120">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="4cb6f-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="4cb6f-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="4cb6f-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="4cb6f-122">Azure 데이터 공유 구독 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4cb6f-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="4cb6f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb6f-123">CommonParameters</span></span>
<span data-ttu-id="4cb6f-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb6f-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4cb6f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb6f-126">입력</span><span class="sxs-lookup"><span data-stu-id="4cb6f-126">INPUTS</span></span>

### <span data-ttu-id="4cb6f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4cb6f-127">System.String</span></span>

## <span data-ttu-id="4cb6f-128">출력</span><span class="sxs-lookup"><span data-stu-id="4cb6f-128">OUTPUTS</span></span>

### <span data-ttu-id="4cb6f-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="4cb6f-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="4cb6f-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4cb6f-130">NOTES</span></span>

## <span data-ttu-id="4cb6f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cb6f-131">RELATED LINKS</span></span>
