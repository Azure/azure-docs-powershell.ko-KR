---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 5dbf797ffabdf42b1d30d9d709ba6bb3153d8696
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324393"
---
# <span data-ttu-id="58f56-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="58f56-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="58f56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58f56-102">SYNOPSIS</span></span>
<span data-ttu-id="58f56-103">Azure 데이터 공유에 데이터 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="58f56-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="58f56-104">구문</span><span class="sxs-lookup"><span data-stu-id="58f56-104">SYNTAX</span></span>

### <span data-ttu-id="58f56-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="58f56-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f56-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="58f56-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f56-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="58f56-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f56-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="58f56-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58f56-109">설명</span><span class="sxs-lookup"><span data-stu-id="58f56-109">DESCRIPTION</span></span>
<span data-ttu-id="58f56-110">**New-AzDataShareDataSet** cmdlet은 데이터 공유 계정의 Azure 데이터 공유에 데이터 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="58f56-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="58f56-111">Blob, ADLS Gen2 및 ADLS Gen1 형식의 데이터 집합을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58f56-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="58f56-112">예제</span><span class="sxs-lookup"><span data-stu-id="58f56-112">EXAMPLES</span></span>

### <span data-ttu-id="58f56-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="58f56-113">Example 1</span></span>
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

<span data-ttu-id="58f56-114">이 명령은 Azure 데이터 공유 AdsShare에 Blob 컨테이너 형식의 AdsDataSet이라는 데이터 세트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="58f56-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="58f56-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58f56-115">PARAMETERS</span></span>

### <span data-ttu-id="58f56-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58f56-116">-AccountName</span></span>
<span data-ttu-id="58f56-117">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="58f56-117">Azure data share account name</span></span>

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

### <span data-ttu-id="58f56-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="58f56-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="58f56-119">Azure Storage ADLS gen1 폴더 경로</span><span class="sxs-lookup"><span data-stu-id="58f56-119">Azure storage ADLS gen1 folder path</span></span>

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

### <span data-ttu-id="58f56-120">-Container</span><span class="sxs-lookup"><span data-stu-id="58f56-120">-Container</span></span>
<span data-ttu-id="58f56-121">Azure Storage 계정 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="58f56-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="58f56-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f56-122">-DefaultProfile</span></span>
<span data-ttu-id="58f56-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58f56-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58f56-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="58f56-124">-FileName</span></span>
<span data-ttu-id="58f56-125">Azure Storage ADLS gen1 파일 이름</span><span class="sxs-lookup"><span data-stu-id="58f56-125">Azure storage ADLS gen1 file name</span></span>

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

### <span data-ttu-id="58f56-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="58f56-126">-FilePath</span></span>
<span data-ttu-id="58f56-127">Azure 저장소 파일 경로</span><span class="sxs-lookup"><span data-stu-id="58f56-127">Azure storage file path</span></span>

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

### <span data-ttu-id="58f56-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="58f56-128">-FileSystem</span></span>
<span data-ttu-id="58f56-129">Azure ADLS gen2 파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="58f56-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="58f56-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="58f56-130">-FolderPath</span></span>
<span data-ttu-id="58f56-131">Azure Storage 폴더 경로</span><span class="sxs-lookup"><span data-stu-id="58f56-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="58f56-132">-Name</span><span class="sxs-lookup"><span data-stu-id="58f56-132">-Name</span></span>
<span data-ttu-id="58f56-133">Azure 데이터 집합 이름</span><span class="sxs-lookup"><span data-stu-id="58f56-133">Azure data set name</span></span>

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

### <span data-ttu-id="58f56-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58f56-134">-ResourceGroupName</span></span>
<span data-ttu-id="58f56-135">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="58f56-135">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="58f56-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="58f56-136">-ShareName</span></span>
<span data-ttu-id="58f56-137">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="58f56-137">Azure data share name</span></span>

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

### <span data-ttu-id="58f56-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="58f56-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="58f56-139">Azure Storage 계정 resourceId</span><span class="sxs-lookup"><span data-stu-id="58f56-139">Azure storage account resourceId</span></span>

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

### <span data-ttu-id="58f56-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58f56-140">-Confirm</span></span>
<span data-ttu-id="58f56-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="58f56-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58f56-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f56-142">-WhatIf</span></span>
<span data-ttu-id="58f56-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="58f56-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58f56-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58f56-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58f56-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f56-145">CommonParameters</span></span>
<span data-ttu-id="58f56-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="58f56-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f56-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58f56-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f56-148">입력</span><span class="sxs-lookup"><span data-stu-id="58f56-148">INPUTS</span></span>

### <span data-ttu-id="58f56-149">System.String</span><span class="sxs-lookup"><span data-stu-id="58f56-149">System.String</span></span>

## <span data-ttu-id="58f56-150">출력</span><span class="sxs-lookup"><span data-stu-id="58f56-150">OUTPUTS</span></span>

### <span data-ttu-id="58f56-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="58f56-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="58f56-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="58f56-152">NOTES</span></span>

## <span data-ttu-id="58f56-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58f56-153">RELATED LINKS</span></span>
