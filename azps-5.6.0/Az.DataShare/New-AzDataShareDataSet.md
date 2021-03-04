---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 12c0c4832d13e3e8637ab1cdb36a1f3fe3abb7d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969232"
---
# <span data-ttu-id="8e4f1-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8e4f1-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="8e4f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4f1-103">Azure 데이터 공유에 데이터 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="8e4f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e4f1-104">SYNTAX</span></span>

### <span data-ttu-id="8e4f1-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8e4f1-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4f1-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="8e4f1-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4f1-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e4f1-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4f1-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e4f1-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e4f1-109">설명</span><span class="sxs-lookup"><span data-stu-id="8e4f1-109">DESCRIPTION</span></span>
<span data-ttu-id="8e4f1-110">**New-AzDataShareDataSet** cmdlet은 데이터 공유 계정의 Azure 데이터 공유에 데이터 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="8e4f1-111">Blob, ADLS Gen2 및 ADLS Gen1 형식의 데이터 집합을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="8e4f1-112">예제</span><span class="sxs-lookup"><span data-stu-id="8e4f1-112">EXAMPLES</span></span>

### <span data-ttu-id="8e4f1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e4f1-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="8e4f1-114">이 명령은 Azure 데이터 공유 AdsShare에 형식 Blob 컨테이너의 AdsDataSet이라는 데이터 세트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="8e4f1-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e4f1-115">PARAMETERS</span></span>

### <span data-ttu-id="8e4f1-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e4f1-116">-AccountName</span></span>
<span data-ttu-id="8e4f1-117">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="8e4f1-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4f1-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="8e4f1-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="8e4f1-119">Azure Storage ADLS gen1 폴더 경로</span><span class="sxs-lookup"><span data-stu-id="8e4f1-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4f1-120">-Container</span><span class="sxs-lookup"><span data-stu-id="8e4f1-120">-Container</span></span>
<span data-ttu-id="8e4f1-121">Azure Storage 계정 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="8e4f1-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="8e4f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e4f1-122">-DefaultProfile</span></span>
<span data-ttu-id="8e4f1-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e4f1-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="8e4f1-124">-FileName</span></span>
<span data-ttu-id="8e4f1-125">Azure Storage ADLS gen1 파일 이름</span><span class="sxs-lookup"><span data-stu-id="8e4f1-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4f1-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="8e4f1-126">-FilePath</span></span>
<span data-ttu-id="8e4f1-127">Azure Storage 파일 경로</span><span class="sxs-lookup"><span data-stu-id="8e4f1-127">Azure storage file path</span></span>

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

### <span data-ttu-id="8e4f1-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="8e4f1-128">-FileSystem</span></span>
<span data-ttu-id="8e4f1-129">Azure ADLS gen2 파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="8e4f1-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="8e4f1-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="8e4f1-130">-FolderPath</span></span>
<span data-ttu-id="8e4f1-131">Azure Storage 폴더 경로</span><span class="sxs-lookup"><span data-stu-id="8e4f1-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="8e4f1-132">-Name</span><span class="sxs-lookup"><span data-stu-id="8e4f1-132">-Name</span></span>
<span data-ttu-id="8e4f1-133">Azure 데이터 집합 이름</span><span class="sxs-lookup"><span data-stu-id="8e4f1-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4f1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e4f1-134">-ResourceGroupName</span></span>
<span data-ttu-id="8e4f1-135">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8e4f1-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4f1-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8e4f1-136">-ShareName</span></span>
<span data-ttu-id="8e4f1-137">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="8e4f1-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4f1-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8e4f1-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="8e4f1-139">Azure Storage 계정 resourceId</span><span class="sxs-lookup"><span data-stu-id="8e4f1-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e4f1-140">-확인</span><span class="sxs-lookup"><span data-stu-id="8e4f1-140">-Confirm</span></span>
<span data-ttu-id="8e4f1-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e4f1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e4f1-142">-WhatIf</span></span>
<span data-ttu-id="8e4f1-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e4f1-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e4f1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4f1-145">CommonParameters</span></span>
<span data-ttu-id="8e4f1-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e4f1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4f1-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e4f1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4f1-148">입력</span><span class="sxs-lookup"><span data-stu-id="8e4f1-148">INPUTS</span></span>

### <span data-ttu-id="8e4f1-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8e4f1-149">System.String</span></span>

## <span data-ttu-id="8e4f1-150">출력</span><span class="sxs-lookup"><span data-stu-id="8e4f1-150">OUTPUTS</span></span>

### <span data-ttu-id="8e4f1-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8e4f1-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="8e4f1-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e4f1-152">NOTES</span></span>

## <span data-ttu-id="8e4f1-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e4f1-153">RELATED LINKS</span></span>
