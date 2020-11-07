---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 0c591a60e1a7b1a5b5d20e7a4747bc8c08389816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696741"
---
# <span data-ttu-id="4a108-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="4a108-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="4a108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a108-102">SYNOPSIS</span></span>
<span data-ttu-id="4a108-103">Azure data share의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="4a108-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a108-104">SYNTAX</span></span>

### <span data-ttu-id="4a108-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4a108-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a108-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a108-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a108-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4a108-107">DESCRIPTION</span></span>
<span data-ttu-id="4a108-108">**AzDataShareDataSet** Cmdlet은 Azure data 공유 계정의 공유에 추가 된 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="4a108-109">데이터 집합의 이름을 지정 하는 경우이 cmdlet은 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="4a108-110">이름을 지정 하지 않으면이 cmdlet은 공유의 모든 데이터 집합에 대 한 정보를 가져옵니다. 칼럼</span><span class="sxs-lookup"><span data-stu-id="4a108-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="4a108-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4a108-111">EXAMPLES</span></span>

### <span data-ttu-id="4a108-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a108-112">Example 1</span></span>
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

<span data-ttu-id="4a108-113">이 명령은 Azure data share 계정 WikiAdsAccount 및 리소스 그룹 광고에서 공유 Adsdataset의 AdsDataSet 데이터 집합에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="4a108-114">변수</span><span class="sxs-lookup"><span data-stu-id="4a108-114">PARAMETERS</span></span>

### <span data-ttu-id="4a108-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a108-115">-AccountName</span></span>
<span data-ttu-id="4a108-116">Azure data share 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="4a108-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a108-117">-DefaultProfile</span></span>
<span data-ttu-id="4a108-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a108-119">-이름</span><span class="sxs-lookup"><span data-stu-id="4a108-119">-Name</span></span>
<span data-ttu-id="4a108-120">Azure 데이터 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-120">Azure data set name.</span></span>

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

### <span data-ttu-id="4a108-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a108-121">-ResourceGroupName</span></span>
<span data-ttu-id="4a108-122">Azure data share 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="4a108-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a108-123">-ResourceId</span></span>
<span data-ttu-id="4a108-124">Azure 데이터 집합의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="4a108-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4a108-125">-ShareName</span></span>
<span data-ttu-id="4a108-126">Azure 데이터 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-126">Azure data share name.</span></span>

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

### <span data-ttu-id="4a108-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a108-127">CommonParameters</span></span>
<span data-ttu-id="4a108-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a108-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a108-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a108-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a108-130">입력</span><span class="sxs-lookup"><span data-stu-id="4a108-130">INPUTS</span></span>

### <span data-ttu-id="4a108-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4a108-131">System.String</span></span>

## <span data-ttu-id="4a108-132">출력</span><span class="sxs-lookup"><span data-stu-id="4a108-132">OUTPUTS</span></span>

### <span data-ttu-id="4a108-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="4a108-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="4a108-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4a108-134">NOTES</span></span>

## <span data-ttu-id="4a108-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a108-135">RELATED LINKS</span></span>
