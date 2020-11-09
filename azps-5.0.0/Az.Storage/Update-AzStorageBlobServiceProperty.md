---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309417"
---
# <span data-ttu-id="67e58-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="67e58-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="67e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67e58-102">SYNOPSIS</span></span>
<span data-ttu-id="67e58-103">Azure 저장소 Blob 서비스에 대 한 서비스 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="67e58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67e58-104">SYNTAX</span></span>

### <span data-ttu-id="67e58-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="67e58-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e58-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="67e58-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e58-107">Blobservice속성 Resourceid</span><span class="sxs-lookup"><span data-stu-id="67e58-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e58-108">설명은</span><span class="sxs-lookup"><span data-stu-id="67e58-108">DESCRIPTION</span></span>
<span data-ttu-id="67e58-109">**AzStorageBlobServiceProperty** Cmdlet은 Azure Storage Blob 서비스에 대 한 서비스 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="67e58-110">예제의</span><span class="sxs-lookup"><span data-stu-id="67e58-110">EXAMPLES</span></span>

### <span data-ttu-id="67e58-111">예제 1: Blob service DefaultServiceVersion을 2018-03-28로 설정</span><span class="sxs-lookup"><span data-stu-id="67e58-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
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

<span data-ttu-id="67e58-112">이 명령은 DefaultServiceVersion Blob 서비스를 2018-03-28으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="67e58-113">예제 2: 저장소 계정의 Blob 서비스에서 Changefeed 사용</span><span class="sxs-lookup"><span data-stu-id="67e58-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
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

<span data-ttu-id="67e58-114">이 명령은 저장소 계정의 Blob 서비스에서 변경 피드를 사용 하도록 설정 합니다. Azure Blob Storage에서 GPv2 또는 Blob 저장소 계정으로 수신 대기 하 여 blob 수준 만들기, 수정 또는 삭제 이벤트에 대 한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="67e58-115">그런 다음 저장소 계정 내의 $blobchangefeed 컨테이너에 저장 된 blob에 대 한 순서가 지정 된 이벤트 로그를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="67e58-116">Serialize 된 변경 내용은 Apache Avro 파일로 유지 되며 비동기적으로 처리 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="67e58-117">예제 3: 저장소 계정의 Blob 서비스에서 버전 관리 사용</span><span class="sxs-lookup"><span data-stu-id="67e58-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
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

<span data-ttu-id="67e58-118">이 명령은 저장소 계정의 Blob 서비스에서 버전 관리를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="67e58-119">변수</span><span class="sxs-lookup"><span data-stu-id="67e58-119">PARAMETERS</span></span>

### <span data-ttu-id="67e58-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e58-120">-DefaultProfile</span></span>
<span data-ttu-id="67e58-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67e58-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="67e58-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="67e58-123">설정할 기본 서비스 버전</span><span class="sxs-lookup"><span data-stu-id="67e58-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="67e58-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="67e58-124">-EnableChangeFeed</span></span>
<span data-ttu-id="67e58-125">$True으로 설정 하 여 저장소 계정에 대 한 변경 피드 로깅을 사용 하도록 설정 하 고, $false로 설정한 피드 로깅 설정을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

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

### <span data-ttu-id="67e58-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="67e58-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="67e58-127">True로 설정 된 경우 버전 관리를 사용 하도록 설정 하 여 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-127">Gets or sets versioning is enabled if set to true.</span></span>

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

### <span data-ttu-id="67e58-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e58-128">-ResourceGroupName</span></span>
<span data-ttu-id="67e58-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="67e58-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67e58-130">-ResourceId</span></span>
<span data-ttu-id="67e58-131">저장소 계정 리소스 Id 또는 Blob 서비스 속성 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="67e58-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="67e58-132">-StorageAccount</span></span>
<span data-ttu-id="67e58-133">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="67e58-133">Storage account object</span></span>

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

### <span data-ttu-id="67e58-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="67e58-134">-StorageAccountName</span></span>
<span data-ttu-id="67e58-135">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="67e58-136">-확인</span><span class="sxs-lookup"><span data-stu-id="67e58-136">-Confirm</span></span>
<span data-ttu-id="67e58-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e58-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e58-138">-WhatIf</span></span>
<span data-ttu-id="67e58-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67e58-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67e58-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e58-141">CommonParameters</span></span>
<span data-ttu-id="67e58-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67e58-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e58-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e58-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e58-144">입력</span><span class="sxs-lookup"><span data-stu-id="67e58-144">INPUTS</span></span>

### <span data-ttu-id="67e58-145">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67e58-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="67e58-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67e58-146">System.String</span></span>

## <span data-ttu-id="67e58-147">출력</span><span class="sxs-lookup"><span data-stu-id="67e58-147">OUTPUTS</span></span>

### <span data-ttu-id="67e58-148">Microsoft. a. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="67e58-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="67e58-149">상속자</span><span class="sxs-lookup"><span data-stu-id="67e58-149">NOTES</span></span>

## <span data-ttu-id="67e58-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67e58-150">RELATED LINKS</span></span>
