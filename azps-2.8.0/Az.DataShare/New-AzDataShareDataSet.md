---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 9478e4892d4d7effdf37b7312f82348a2e8ea03a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696712"
---
# <span data-ttu-id="f8b01-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="f8b01-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="f8b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8b01-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b01-103">Azure data share에 데이터 집합을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b01-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="f8b01-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8b01-104">SYNTAX</span></span>

### <span data-ttu-id="f8b01-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f8b01-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b01-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="f8b01-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b01-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8b01-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8b01-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8b01-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8b01-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f8b01-109">DESCRIPTION</span></span>
<span data-ttu-id="f8b01-110">Data 공유 계정의 azure data share에서 **AzDataShareDataSet** cmdlet이 데이터 집합을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b01-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="f8b01-111">Blob, ADLS Gen2 및 ADLS Gen1 유형의 데이터 집합을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8b01-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="f8b01-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f8b01-112">EXAMPLES</span></span>

### <span data-ttu-id="f8b01-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8b01-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="f8b01-114">이 명령은 형식 blob 컨테이너의 AdsDataSet 이라는 데이터 집합을 azure data 공유 Adsdataset에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b01-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="f8b01-115">변수</span><span class="sxs-lookup"><span data-stu-id="f8b01-115">PARAMETERS</span></span>

### <span data-ttu-id="f8b01-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f8b01-116">-AccountName</span></span>
<span data-ttu-id="f8b01-117">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="f8b01-117">Azure data share account name</span></span>

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

### <span data-ttu-id="f8b01-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="f8b01-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="f8b01-119">Azure storage ADLS gen1 폴더 경로</span><span class="sxs-lookup"><span data-stu-id="f8b01-119">Azure storage ADLS gen1 folder path</span></span>

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

### <span data-ttu-id="f8b01-120">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="f8b01-120">-Container</span></span>
<span data-ttu-id="f8b01-121">Azure storage 계정 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="f8b01-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="f8b01-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b01-122">-DefaultProfile</span></span>
<span data-ttu-id="f8b01-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8b01-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8b01-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="f8b01-124">-FileName</span></span>
<span data-ttu-id="f8b01-125">Azure storage ADLS gen1 파일 이름</span><span class="sxs-lookup"><span data-stu-id="f8b01-125">Azure storage ADLS gen1 file name</span></span>

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

### <span data-ttu-id="f8b01-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="f8b01-126">-FilePath</span></span>
<span data-ttu-id="f8b01-127">Azure 저장소 파일 경로</span><span class="sxs-lookup"><span data-stu-id="f8b01-127">Azure storage file path</span></span>

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

### <span data-ttu-id="f8b01-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="f8b01-128">-FileSystem</span></span>
<span data-ttu-id="f8b01-129">Azure ADLS gen2 파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="f8b01-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="f8b01-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="f8b01-130">-FolderPath</span></span>
<span data-ttu-id="f8b01-131">Azure 저장소 폴더 경로</span><span class="sxs-lookup"><span data-stu-id="f8b01-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="f8b01-132">-이름</span><span class="sxs-lookup"><span data-stu-id="f8b01-132">-Name</span></span>
<span data-ttu-id="f8b01-133">Azure 데이터 집합 이름</span><span class="sxs-lookup"><span data-stu-id="f8b01-133">Azure data set name</span></span>

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

### <span data-ttu-id="f8b01-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b01-134">-ResourceGroupName</span></span>
<span data-ttu-id="f8b01-135">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f8b01-135">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f8b01-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f8b01-136">-ShareName</span></span>
<span data-ttu-id="f8b01-137">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="f8b01-137">Azure data share name</span></span>

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

### <span data-ttu-id="f8b01-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f8b01-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="f8b01-139">Azure 저장소 계정 resourceId</span><span class="sxs-lookup"><span data-stu-id="f8b01-139">Azure storage account resourceId</span></span>

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

### <span data-ttu-id="f8b01-140">-확인</span><span class="sxs-lookup"><span data-stu-id="f8b01-140">-Confirm</span></span>
<span data-ttu-id="f8b01-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b01-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b01-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8b01-142">-WhatIf</span></span>
<span data-ttu-id="f8b01-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8b01-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8b01-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8b01-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b01-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b01-145">CommonParameters</span></span>
<span data-ttu-id="f8b01-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8b01-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b01-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b01-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b01-148">입력</span><span class="sxs-lookup"><span data-stu-id="f8b01-148">INPUTS</span></span>

### <span data-ttu-id="f8b01-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f8b01-149">System.String</span></span>

## <span data-ttu-id="f8b01-150">출력</span><span class="sxs-lookup"><span data-stu-id="f8b01-150">OUTPUTS</span></span>

### <span data-ttu-id="f8b01-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="f8b01-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="f8b01-152">상속자</span><span class="sxs-lookup"><span data-stu-id="f8b01-152">NOTES</span></span>

## <span data-ttu-id="f8b01-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8b01-153">RELATED LINKS</span></span>
