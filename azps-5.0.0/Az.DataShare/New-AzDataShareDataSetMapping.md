---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305198"
---
# <span data-ttu-id="9901d-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="9901d-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="9901d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9901d-102">SYNOPSIS</span></span>
<span data-ttu-id="9901d-103">공유 구독에 대 한 데이터 집합 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9901d-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="9901d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9901d-104">SYNTAX</span></span>

### <span data-ttu-id="9901d-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9901d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9901d-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="9901d-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9901d-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="9901d-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9901d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9901d-108">DESCRIPTION</span></span>
<span data-ttu-id="9901d-109">**AzDataShareDataSetMapping** cmdlet은 공유 구독의 원본 데이터 집합 및 싱크 저장소 계정 간에 데이터 집합 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9901d-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="9901d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9901d-110">EXAMPLES</span></span>

### <span data-ttu-id="9901d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9901d-111">Example 1</span></span>
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

<span data-ttu-id="9901d-112">이 명령은 데이터 공유 계정 WikiAdsAccount에서 구독 공유 AdsShareSubscription 저장소 계정 AdsStorage에 대 한 AdsDataSetMapping 데이터 집합 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9901d-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="9901d-113">변수</span><span class="sxs-lookup"><span data-stu-id="9901d-113">PARAMETERS</span></span>

### <span data-ttu-id="9901d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9901d-114">-AccountName</span></span>
<span data-ttu-id="9901d-115">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="9901d-115">Azure data share account name</span></span>

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

### <span data-ttu-id="9901d-116">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="9901d-116">-Container</span></span>
<span data-ttu-id="9901d-117">Azure storage 계정 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="9901d-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="9901d-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="9901d-118">-DataSetId</span></span>
<span data-ttu-id="9901d-119">소비자 데이터 집합 id</span><span class="sxs-lookup"><span data-stu-id="9901d-119">Consumer data set id</span></span>

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

### <span data-ttu-id="9901d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9901d-120">-DefaultProfile</span></span>
<span data-ttu-id="9901d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9901d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9901d-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="9901d-122">-FilePath</span></span>
<span data-ttu-id="9901d-123">Azure 저장소 파일 경로</span><span class="sxs-lookup"><span data-stu-id="9901d-123">Azure storage file path</span></span>

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

### <span data-ttu-id="9901d-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="9901d-124">-FileSystem</span></span>
<span data-ttu-id="9901d-125">Azure ADLS gen2 파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="9901d-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="9901d-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="9901d-126">-FolderPath</span></span>
<span data-ttu-id="9901d-127">Azure 저장소 폴더 경로</span><span class="sxs-lookup"><span data-stu-id="9901d-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="9901d-128">-이름</span><span class="sxs-lookup"><span data-stu-id="9901d-128">-Name</span></span>
<span data-ttu-id="9901d-129">Azure 데이터 집합 매핑 이름</span><span class="sxs-lookup"><span data-stu-id="9901d-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="9901d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9901d-130">-ResourceGroupName</span></span>
<span data-ttu-id="9901d-131">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9901d-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9901d-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9901d-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="9901d-133">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="9901d-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="9901d-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9901d-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="9901d-135">Azure 저장소 계정 ResourceId</span><span class="sxs-lookup"><span data-stu-id="9901d-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="9901d-136">-확인</span><span class="sxs-lookup"><span data-stu-id="9901d-136">-Confirm</span></span>
<span data-ttu-id="9901d-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9901d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9901d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9901d-138">-WhatIf</span></span>
<span data-ttu-id="9901d-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9901d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9901d-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9901d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9901d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9901d-141">CommonParameters</span></span>
<span data-ttu-id="9901d-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9901d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9901d-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9901d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9901d-144">입력</span><span class="sxs-lookup"><span data-stu-id="9901d-144">INPUTS</span></span>

### <span data-ttu-id="9901d-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9901d-145">System.String</span></span>

## <span data-ttu-id="9901d-146">출력</span><span class="sxs-lookup"><span data-stu-id="9901d-146">OUTPUTS</span></span>

### <span data-ttu-id="9901d-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="9901d-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="9901d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="9901d-148">NOTES</span></span>

## <span data-ttu-id="9901d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9901d-149">RELATED LINKS</span></span>
