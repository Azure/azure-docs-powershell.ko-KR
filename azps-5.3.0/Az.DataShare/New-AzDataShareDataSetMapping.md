---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377245"
---
# <span data-ttu-id="61f15-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="61f15-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="61f15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f15-102">SYNOPSIS</span></span>
<span data-ttu-id="61f15-103">공유 구독에 대한 데이터 집합 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61f15-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="61f15-104">구문</span><span class="sxs-lookup"><span data-stu-id="61f15-104">SYNTAX</span></span>

### <span data-ttu-id="61f15-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="61f15-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61f15-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="61f15-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f15-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="61f15-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61f15-108">설명</span><span class="sxs-lookup"><span data-stu-id="61f15-108">DESCRIPTION</span></span>
<span data-ttu-id="61f15-109">**New-AzDataShareDataSetMapping** cmdlet은 공유 구독의 원본 데이터 집합과 싱크 저장소 계정 간의 데이터 집합 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61f15-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="61f15-110">예제</span><span class="sxs-lookup"><span data-stu-id="61f15-110">EXAMPLES</span></span>

### <span data-ttu-id="61f15-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="61f15-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="61f15-112">이 명령은 데이터 공유 계정 WikiAdsAccount의 공유 구독 AdsShareSubscription에 대한 Storage 계정 AdsStorage에 AdsDataSetMapping을 매핑하는 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61f15-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="61f15-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61f15-113">PARAMETERS</span></span>

### <span data-ttu-id="61f15-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61f15-114">-AccountName</span></span>
<span data-ttu-id="61f15-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="61f15-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-116">-Container</span><span class="sxs-lookup"><span data-stu-id="61f15-116">-Container</span></span>
<span data-ttu-id="61f15-117">Azure Storage 계정 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="61f15-117">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="61f15-118">-DataSetId</span></span>
<span data-ttu-id="61f15-119">소비자 데이터 집합 ID</span><span class="sxs-lookup"><span data-stu-id="61f15-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f15-120">-DefaultProfile</span></span>
<span data-ttu-id="61f15-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61f15-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61f15-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="61f15-122">-FilePath</span></span>
<span data-ttu-id="61f15-123">Azure 저장소 파일 경로</span><span class="sxs-lookup"><span data-stu-id="61f15-123">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="61f15-124">-FileSystem</span></span>
<span data-ttu-id="61f15-125">Azure ADLS gen2 파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="61f15-125">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="61f15-126">-FolderPath</span></span>
<span data-ttu-id="61f15-127">Azure Storage 폴더 경로</span><span class="sxs-lookup"><span data-stu-id="61f15-127">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-128">-Name</span><span class="sxs-lookup"><span data-stu-id="61f15-128">-Name</span></span>
<span data-ttu-id="61f15-129">Azure 데이터 집합 매핑 이름</span><span class="sxs-lookup"><span data-stu-id="61f15-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f15-130">-ResourceGroupName</span></span>
<span data-ttu-id="61f15-131">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="61f15-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="61f15-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="61f15-133">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="61f15-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="61f15-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="61f15-135">Azure Storage 계정 ResourceId</span><span class="sxs-lookup"><span data-stu-id="61f15-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61f15-136">-Confirm</span></span>
<span data-ttu-id="61f15-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="61f15-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f15-138">-WhatIf</span></span>
<span data-ttu-id="61f15-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="61f15-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f15-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61f15-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f15-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f15-141">CommonParameters</span></span>
<span data-ttu-id="61f15-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61f15-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f15-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61f15-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f15-144">입력</span><span class="sxs-lookup"><span data-stu-id="61f15-144">INPUTS</span></span>

### <span data-ttu-id="61f15-145">System.String</span><span class="sxs-lookup"><span data-stu-id="61f15-145">System.String</span></span>

## <span data-ttu-id="61f15-146">출력</span><span class="sxs-lookup"><span data-stu-id="61f15-146">OUTPUTS</span></span>

### <span data-ttu-id="61f15-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="61f15-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="61f15-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61f15-148">NOTES</span></span>

## <span data-ttu-id="61f15-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61f15-149">RELATED LINKS</span></span>
