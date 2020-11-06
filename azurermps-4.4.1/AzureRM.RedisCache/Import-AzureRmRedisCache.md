---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: 792a76d024b34dd90fd8818303c61daafeb4f46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529189"
---
# <span data-ttu-id="178d3-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="178d3-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="178d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="178d3-102">SYNOPSIS</span></span>
<span data-ttu-id="178d3-103">Blob에서 Azure Redis Cache로 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="178d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="178d3-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="178d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="178d3-105">DESCRIPTION</span></span>
<span data-ttu-id="178d3-106">**AzureRmRedisCache** cmdlet은 Blob에서 Azure Redis Cache로 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="178d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="178d3-107">EXAMPLES</span></span>

### <span data-ttu-id="178d3-108">예제 1: 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="178d3-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="178d3-109">이 명령은 SAS URL로 지정 된 blob에서 Azure Redis Cache로 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="178d3-110">변수</span><span class="sxs-lookup"><span data-stu-id="178d3-110">PARAMETERS</span></span>

### <span data-ttu-id="178d3-111">-파일</span><span class="sxs-lookup"><span data-stu-id="178d3-111">-Files</span></span>
<span data-ttu-id="178d3-112">이 cmdlet이 캐시로 가져오는 콘텐츠가 있는 blob의 SAS Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-112">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="178d3-113">다음 PowerShell 명령을 사용 하 여 SAS Url을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-113">You can generate the SAS URLs using the following PowerShell commands:</span></span>

<span data-ttu-id="178d3-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "key"</span><span class="sxs-lookup"><span data-stu-id="178d3-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="178d3-115">$sasKeyForBlob = New-AzureStorageBlobSASToken-컨테이너 "containerName"-blob "blobName"-Permission "rwdl"-StartTime ([System: DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-Context $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="178d3-115">$sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span>

<span data-ttu-id="178d3-116">Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-Files ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="178d3-116">Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178d3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="178d3-117">-Force</span></span>
<span data-ttu-id="178d3-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178d3-119">-형식</span><span class="sxs-lookup"><span data-stu-id="178d3-119">-Format</span></span>
<span data-ttu-id="178d3-120">Blob 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-120">Specifies the format of the blob.</span></span>
<span data-ttu-id="178d3-121">현재 rdb만 지원 되는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-121">Currently rdb is the only supported format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178d3-122">-이름</span><span class="sxs-lookup"><span data-stu-id="178d3-122">-Name</span></span>
<span data-ttu-id="178d3-123">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-123">Specifies the name of a cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178d3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="178d3-124">-PassThru</span></span>
<span data-ttu-id="178d3-125">이 cmdlet이 작업 성공 여부를 나타내는 Boolean을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-125">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="178d3-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="178d3-128">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-128">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178d3-129">-확인</span><span class="sxs-lookup"><span data-stu-id="178d3-129">-Confirm</span></span>
<span data-ttu-id="178d3-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="178d3-131">-WhatIf</span></span>
<span data-ttu-id="178d3-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="178d3-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178d3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178d3-134">-DefaultProfile</span></span>
<span data-ttu-id="178d3-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178d3-136">CommonParameters</span></span>
<span data-ttu-id="178d3-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178d3-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178d3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178d3-139">입력</span><span class="sxs-lookup"><span data-stu-id="178d3-139">INPUTS</span></span>

### <span data-ttu-id="178d3-140">않아야</span><span class="sxs-lookup"><span data-stu-id="178d3-140">None</span></span>
<span data-ttu-id="178d3-141">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="178d3-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="178d3-142">출력</span><span class="sxs-lookup"><span data-stu-id="178d3-142">OUTPUTS</span></span>

### <span data-ttu-id="178d3-143">않아야</span><span class="sxs-lookup"><span data-stu-id="178d3-143">None</span></span>

## <span data-ttu-id="178d3-144">상속자</span><span class="sxs-lookup"><span data-stu-id="178d3-144">NOTES</span></span>
* <span data-ttu-id="178d3-145">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="178d3-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="178d3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="178d3-146">RELATED LINKS</span></span>

[<span data-ttu-id="178d3-147">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="178d3-147">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="178d3-148">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="178d3-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="178d3-149">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="178d3-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="178d3-150">다시 설정-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="178d3-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="178d3-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="178d3-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


