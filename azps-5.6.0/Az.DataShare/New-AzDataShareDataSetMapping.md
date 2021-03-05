---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 56c573f6806acf2d9c45f583bbbb880aa6fc5638
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996739"
---
# <span data-ttu-id="6bff6-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="6bff6-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="6bff6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bff6-102">SYNOPSIS</span></span>
<span data-ttu-id="6bff6-103">공유 구독에 대한 데이터 집합 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6bff6-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="6bff6-104">구문</span><span class="sxs-lookup"><span data-stu-id="6bff6-104">SYNTAX</span></span>

### <span data-ttu-id="6bff6-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6bff6-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bff6-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="6bff6-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bff6-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bff6-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bff6-108">설명</span><span class="sxs-lookup"><span data-stu-id="6bff6-108">DESCRIPTION</span></span>
<span data-ttu-id="6bff6-109">**New-AzDataShareDataSetMapping** cmdlet은 공유 구독에서 원본 데이터 집합과 싱크 저장소 계정 간에 데이터 집합 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6bff6-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="6bff6-110">예제</span><span class="sxs-lookup"><span data-stu-id="6bff6-110">EXAMPLES</span></span>

### <span data-ttu-id="6bff6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6bff6-111">Example 1</span></span>
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

<span data-ttu-id="6bff6-112">이 명령은 데이터 공유 계정 WikiAdsAccount에서 공유 구독용 AdsShareSubscription용 Storage 계정 AdsStorage에 AdsDataSetMapping 매핑을 매핑하는 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6bff6-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="6bff6-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6bff6-113">PARAMETERS</span></span>

### <span data-ttu-id="6bff6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6bff6-114">-AccountName</span></span>
<span data-ttu-id="6bff6-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="6bff6-115">Azure data share account name</span></span>

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

### <span data-ttu-id="6bff6-116">-Container</span><span class="sxs-lookup"><span data-stu-id="6bff6-116">-Container</span></span>
<span data-ttu-id="6bff6-117">Azure Storage 계정 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="6bff6-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="6bff6-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="6bff6-118">-DataSetId</span></span>
<span data-ttu-id="6bff6-119">소비자 데이터 세트 ID</span><span class="sxs-lookup"><span data-stu-id="6bff6-119">Consumer data set id</span></span>

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

### <span data-ttu-id="6bff6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bff6-120">-DefaultProfile</span></span>
<span data-ttu-id="6bff6-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6bff6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bff6-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="6bff6-122">-FilePath</span></span>
<span data-ttu-id="6bff6-123">Azure Storage 파일 경로</span><span class="sxs-lookup"><span data-stu-id="6bff6-123">Azure storage file path</span></span>

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

### <span data-ttu-id="6bff6-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="6bff6-124">-FileSystem</span></span>
<span data-ttu-id="6bff6-125">Azure ADLS gen2 파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="6bff6-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="6bff6-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="6bff6-126">-FolderPath</span></span>
<span data-ttu-id="6bff6-127">Azure Storage 폴더 경로</span><span class="sxs-lookup"><span data-stu-id="6bff6-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="6bff6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6bff6-128">-Name</span></span>
<span data-ttu-id="6bff6-129">Azure 데이터 세트 매핑 이름</span><span class="sxs-lookup"><span data-stu-id="6bff6-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="6bff6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bff6-130">-ResourceGroupName</span></span>
<span data-ttu-id="6bff6-131">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6bff6-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6bff6-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6bff6-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="6bff6-133">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="6bff6-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="6bff6-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6bff6-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="6bff6-135">Azure Storage 계정 ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bff6-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="6bff6-136">-확인</span><span class="sxs-lookup"><span data-stu-id="6bff6-136">-Confirm</span></span>
<span data-ttu-id="6bff6-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bff6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bff6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bff6-138">-WhatIf</span></span>
<span data-ttu-id="6bff6-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6bff6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bff6-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bff6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bff6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bff6-141">CommonParameters</span></span>
<span data-ttu-id="6bff6-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6bff6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bff6-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bff6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bff6-144">입력</span><span class="sxs-lookup"><span data-stu-id="6bff6-144">INPUTS</span></span>

### <span data-ttu-id="6bff6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="6bff6-145">System.String</span></span>

## <span data-ttu-id="6bff6-146">출력</span><span class="sxs-lookup"><span data-stu-id="6bff6-146">OUTPUTS</span></span>

### <span data-ttu-id="6bff6-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="6bff6-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="6bff6-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6bff6-148">NOTES</span></span>

## <span data-ttu-id="6bff6-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bff6-149">RELATED LINKS</span></span>
