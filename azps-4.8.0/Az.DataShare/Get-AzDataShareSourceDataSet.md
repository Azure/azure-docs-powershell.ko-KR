---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056394"
---
# <span data-ttu-id="9e347-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="9e347-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="9e347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e347-102">SYNOPSIS</span></span>
<span data-ttu-id="9e347-103">공유 구독의 원본 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e347-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="9e347-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e347-104">SYNTAX</span></span>

### <span data-ttu-id="9e347-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9e347-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e347-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e347-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e347-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9e347-107">DESCRIPTION</span></span>
<span data-ttu-id="9e347-108">**AzDataShareSourceDataSet** cmdlet은 공유 구독의 원본 데이터 집합에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e347-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="9e347-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9e347-109">EXAMPLES</span></span>

### <span data-ttu-id="9e347-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e347-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="9e347-111">원본 공유에서 사용할 수 있는 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e347-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="9e347-112">변수</span><span class="sxs-lookup"><span data-stu-id="9e347-112">PARAMETERS</span></span>

### <span data-ttu-id="9e347-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9e347-113">-AccountName</span></span>
<span data-ttu-id="9e347-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="9e347-114">Azure data share account name</span></span>

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

### <span data-ttu-id="9e347-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e347-115">-DefaultProfile</span></span>
<span data-ttu-id="9e347-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e347-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e347-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e347-117">-ResourceGroupName</span></span>
<span data-ttu-id="9e347-118">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9e347-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9e347-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9e347-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="9e347-120">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="9e347-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="9e347-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="9e347-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="9e347-122">Azure data share 구독 리소스 id</span><span class="sxs-lookup"><span data-stu-id="9e347-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="9e347-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e347-123">CommonParameters</span></span>
<span data-ttu-id="9e347-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e347-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e347-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e347-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e347-126">입력</span><span class="sxs-lookup"><span data-stu-id="9e347-126">INPUTS</span></span>

### <span data-ttu-id="9e347-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9e347-127">System.String</span></span>

## <span data-ttu-id="9e347-128">출력</span><span class="sxs-lookup"><span data-stu-id="9e347-128">OUTPUTS</span></span>

### <span data-ttu-id="9e347-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="9e347-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="9e347-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9e347-130">NOTES</span></span>

## <span data-ttu-id="9e347-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e347-131">RELATED LINKS</span></span>
