---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177057"
---
# <span data-ttu-id="a002a-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a002a-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="a002a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a002a-102">SYNOPSIS</span></span>
<span data-ttu-id="a002a-103">Azure 데이터 공유의 데이터 집합에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="a002a-104">구문</span><span class="sxs-lookup"><span data-stu-id="a002a-104">SYNTAX</span></span>

### <span data-ttu-id="a002a-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a002a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a002a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a002a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a002a-107">설명</span><span class="sxs-lookup"><span data-stu-id="a002a-107">DESCRIPTION</span></span>
<span data-ttu-id="a002a-108">**Get-AzDataShareDataSet** cmdlet은 Azure 데이터 공유 계정의 공유에 추가된 데이터 집합에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="a002a-109">데이터 집합의 이름을 지정하는 경우 이 cmdlet은 데이터 집합에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="a002a-110">이름을 지정하지 않으면 이 cmdlet은 공유의 모든 데이터 집합에 대한 정보를 얻습니다. I</span><span class="sxs-lookup"><span data-stu-id="a002a-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="a002a-111">예제</span><span class="sxs-lookup"><span data-stu-id="a002a-111">EXAMPLES</span></span>

### <span data-ttu-id="a002a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a002a-112">Example 1</span></span>
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

<span data-ttu-id="a002a-113">이 명령은 Azure 데이터 공유 계정 WikiAdsAccount 및 리소스 그룹 ADS의 Share AdsShare에서 AdsDataSet 데이터 집합에 대한 정보를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="a002a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a002a-114">PARAMETERS</span></span>

### <span data-ttu-id="a002a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a002a-115">-AccountName</span></span>
<span data-ttu-id="a002a-116">Azure 데이터 공유 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="a002a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a002a-117">-DefaultProfile</span></span>
<span data-ttu-id="a002a-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a002a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a002a-119">-Name</span></span>
<span data-ttu-id="a002a-120">Azure 데이터 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-120">Azure data set name.</span></span>

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

### <span data-ttu-id="a002a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a002a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a002a-122">Azure 데이터 공유 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="a002a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a002a-123">-ResourceId</span></span>
<span data-ttu-id="a002a-124">Azure 데이터 집합의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="a002a-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a002a-125">-ShareName</span></span>
<span data-ttu-id="a002a-126">Azure 데이터 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-126">Azure data share name.</span></span>

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

### <span data-ttu-id="a002a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a002a-127">CommonParameters</span></span>
<span data-ttu-id="a002a-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a002a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a002a-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a002a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a002a-130">입력</span><span class="sxs-lookup"><span data-stu-id="a002a-130">INPUTS</span></span>

### <span data-ttu-id="a002a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a002a-131">System.String</span></span>

## <span data-ttu-id="a002a-132">출력</span><span class="sxs-lookup"><span data-stu-id="a002a-132">OUTPUTS</span></span>

### <span data-ttu-id="a002a-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a002a-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="a002a-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a002a-134">NOTES</span></span>

## <span data-ttu-id="a002a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a002a-135">RELATED LINKS</span></span>
