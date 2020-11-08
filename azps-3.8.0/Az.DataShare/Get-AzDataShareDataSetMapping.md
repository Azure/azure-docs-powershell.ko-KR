---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: cf8b235d0035955f809b167ba4d532cdae0538c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034175"
---
# <span data-ttu-id="cf22c-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="cf22c-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="cf22c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf22c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf22c-103">공유 구독의 데이터 집합 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="cf22c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf22c-104">SYNTAX</span></span>

### <span data-ttu-id="cf22c-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf22c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf22c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf22c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf22c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cf22c-107">DESCRIPTION</span></span>
<span data-ttu-id="cf22c-108">**AzDataShareDataSetMapping** cmdlet은 이름이 지정 된 경우 특정 데이터 집합 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="cf22c-109">그렇지 않은 경우에는 공유 구독의 모든 데이터 집합 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="cf22c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cf22c-110">EXAMPLES</span></span>

### <span data-ttu-id="cf22c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cf22c-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="cf22c-112">이 명령은 공유 구독의 모든 데이터 집합 매핑에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="cf22c-113">변수</span><span class="sxs-lookup"><span data-stu-id="cf22c-113">PARAMETERS</span></span>

### <span data-ttu-id="cf22c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cf22c-114">-AccountName</span></span>
<span data-ttu-id="cf22c-115">Azure data share 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="cf22c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf22c-116">-DefaultProfile</span></span>
<span data-ttu-id="cf22c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf22c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="cf22c-118">-Name</span></span>
<span data-ttu-id="cf22c-119">Azure 데이터 집합 매핑 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="cf22c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf22c-120">-ResourceGroupName</span></span>
<span data-ttu-id="cf22c-121">Azure data share 계정의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="cf22c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf22c-122">-ResourceId</span></span>
<span data-ttu-id="cf22c-123">Azure 데이터 집합 매핑의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="cf22c-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cf22c-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="cf22c-125">Azure data share 구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="cf22c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf22c-126">CommonParameters</span></span>
<span data-ttu-id="cf22c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf22c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf22c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf22c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf22c-129">입력</span><span class="sxs-lookup"><span data-stu-id="cf22c-129">INPUTS</span></span>

### <span data-ttu-id="cf22c-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cf22c-130">System.String</span></span>

## <span data-ttu-id="cf22c-131">출력</span><span class="sxs-lookup"><span data-stu-id="cf22c-131">OUTPUTS</span></span>

### <span data-ttu-id="cf22c-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="cf22c-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="cf22c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="cf22c-133">NOTES</span></span>

## <span data-ttu-id="cf22c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf22c-134">RELATED LINKS</span></span>
