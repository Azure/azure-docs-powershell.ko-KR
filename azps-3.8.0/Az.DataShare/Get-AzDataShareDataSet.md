---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 73272c2afd0b3d8ef62a522f2e67f04854c2232e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034427"
---
# <span data-ttu-id="8ea1f-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8ea1f-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="8ea1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ea1f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea1f-103">Azure data share의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="8ea1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ea1f-104">SYNTAX</span></span>

### <span data-ttu-id="8ea1f-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ea1f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ea1f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ea1f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ea1f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8ea1f-107">DESCRIPTION</span></span>
<span data-ttu-id="8ea1f-108">**AzDataShareDataSet** Cmdlet은 Azure data 공유 계정의 공유에 추가 된 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="8ea1f-109">데이터 집합의 이름을 지정 하는 경우이 cmdlet은 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="8ea1f-110">이름을 지정 하지 않으면이 cmdlet은 공유의 모든 데이터 집합에 대 한 정보를 가져옵니다. 칼럼</span><span class="sxs-lookup"><span data-stu-id="8ea1f-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="8ea1f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8ea1f-111">EXAMPLES</span></span>

### <span data-ttu-id="8ea1f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ea1f-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="8ea1f-113">이 명령은 Azure data share 계정 WikiAdsAccount 및 리소스 그룹 광고에서 공유 Adsdataset의 AdsDataSet 데이터 집합에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="8ea1f-114">변수</span><span class="sxs-lookup"><span data-stu-id="8ea1f-114">PARAMETERS</span></span>

### <span data-ttu-id="8ea1f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ea1f-115">-AccountName</span></span>
<span data-ttu-id="8ea1f-116">Azure data share 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="8ea1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea1f-117">-DefaultProfile</span></span>
<span data-ttu-id="8ea1f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ea1f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8ea1f-119">-Name</span></span>
<span data-ttu-id="8ea1f-120">Azure 데이터 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-120">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ea1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ea1f-122">Azure data share 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="8ea1f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ea1f-123">-ResourceId</span></span>
<span data-ttu-id="8ea1f-124">Azure 데이터 집합의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="8ea1f-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8ea1f-125">-ShareName</span></span>
<span data-ttu-id="8ea1f-126">Azure 데이터 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-126">Azure data share name.</span></span>

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

### <span data-ttu-id="8ea1f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea1f-127">CommonParameters</span></span>
<span data-ttu-id="8ea1f-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea1f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea1f-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea1f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea1f-130">입력</span><span class="sxs-lookup"><span data-stu-id="8ea1f-130">INPUTS</span></span>

### <span data-ttu-id="8ea1f-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ea1f-131">System.String</span></span>

## <span data-ttu-id="8ea1f-132">출력</span><span class="sxs-lookup"><span data-stu-id="8ea1f-132">OUTPUTS</span></span>

### <span data-ttu-id="8ea1f-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8ea1f-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="8ea1f-134">상속자</span><span class="sxs-lookup"><span data-stu-id="8ea1f-134">NOTES</span></span>

## <span data-ttu-id="8ea1f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ea1f-135">RELATED LINKS</span></span>