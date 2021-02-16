---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197481"
---
# <span data-ttu-id="2c53f-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2c53f-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="2c53f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c53f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c53f-103">Azure Storage Blob service에 대한 서비스 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2c53f-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c53f-104">SYNTAX</span></span>

### <span data-ttu-id="2c53f-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2c53f-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c53f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2c53f-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c53f-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="2c53f-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c53f-108">설명</span><span class="sxs-lookup"><span data-stu-id="2c53f-108">DESCRIPTION</span></span>
<span data-ttu-id="2c53f-109">**Update-AzStorageBlobServiceProperty** cmdlet은 Azure Storage Blob service에 대한 서비스 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2c53f-110">예제</span><span class="sxs-lookup"><span data-stu-id="2c53f-110">EXAMPLES</span></span>

### <span data-ttu-id="2c53f-111">예제 1: Blob service DefaultServiceVersion을 2018-03-28로 설정</span><span class="sxs-lookup"><span data-stu-id="2c53f-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

<span data-ttu-id="2c53f-112">이 명령은 Blob Service의 DefaultServiceVersion을 2018-03-28로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="2c53f-113">예제 2: Storage 계정의 Blob service에서 변경을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="2c53f-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

<span data-ttu-id="2c53f-114">이 명령을 사용하면 Azure Blob Storage에서 Storage 계정 변경 피드 지원의 Blob service에서 변경 피드를 사용할 수 있습니다. 모든 Blob 수준 생성, 수정 또는 삭제 이벤트에 대해 GPv2 또는 Blob Storage 계정을 수신하여 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="2c53f-115">그런 다음 저장소 계정 내의 컨테이너에 저장된 blob에 대한 순서가 $blobchangefeed 로그를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="2c53f-116">직렬화된 변경 내용은 Apache Avro 파일로 유지되고 비동기적으로 증분식으로 처리될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="2c53f-117">예제 3: Storage 계정의 Blob service에서 버전 관리 사용</span><span class="sxs-lookup"><span data-stu-id="2c53f-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

<span data-ttu-id="2c53f-118">이 명령을 사용하면 Storage 계정의 Blob service에서 버전 관리가 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="2c53f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c53f-119">PARAMETERS</span></span>

### <span data-ttu-id="2c53f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c53f-120">-DefaultProfile</span></span>
<span data-ttu-id="2c53f-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c53f-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="2c53f-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="2c53f-123">설정할 기본 서비스 버전</span><span class="sxs-lookup"><span data-stu-id="2c53f-123">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c53f-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="2c53f-124">-EnableChangeFeed</span></span>
<span data-ttu-id="2c53f-125">저장소 계정에 대해 변경 피드 로깅을 사용하도록 설정하고 $true 설정하여 변경 피드 로깅을 사용하지 않도록 $false.</span><span class="sxs-lookup"><span data-stu-id="2c53f-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c53f-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="2c53f-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="2c53f-127">버전이 true로 설정되면 버전이 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-127">Gets or sets versioning is enabled if set to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c53f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c53f-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c53f-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c53f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c53f-130">-ResourceId</span></span>
<span data-ttu-id="2c53f-131">Storage 계정 리소스 ID 또는 Blob service 속성 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c53f-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c53f-132">-StorageAccount</span></span>
<span data-ttu-id="2c53f-133">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="2c53f-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c53f-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2c53f-134">-StorageAccountName</span></span>
<span data-ttu-id="2c53f-135">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c53f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c53f-136">-Confirm</span></span>
<span data-ttu-id="2c53f-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c53f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c53f-138">-WhatIf</span></span>
<span data-ttu-id="2c53f-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2c53f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c53f-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c53f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c53f-141">CommonParameters</span></span>
<span data-ttu-id="2c53f-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c53f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c53f-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2c53f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c53f-144">입력</span><span class="sxs-lookup"><span data-stu-id="2c53f-144">INPUTS</span></span>

### <span data-ttu-id="2c53f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c53f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2c53f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2c53f-146">System.String</span></span>

## <span data-ttu-id="2c53f-147">출력</span><span class="sxs-lookup"><span data-stu-id="2c53f-147">OUTPUTS</span></span>

### <span data-ttu-id="2c53f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="2c53f-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="2c53f-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c53f-149">NOTES</span></span>

## <span data-ttu-id="2c53f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c53f-150">RELATED LINKS</span></span>
