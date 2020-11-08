---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043571"
---
# <span data-ttu-id="9e7b3-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e7b3-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="9e7b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e7b3-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7b3-103">Blob에서 Azure Redis Cache로 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="9e7b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e7b3-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e7b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e7b3-105">DESCRIPTION</span></span>
<span data-ttu-id="9e7b3-106">**AzRedisCache** cmdlet은 Blob에서 Azure Redis Cache로 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="9e7b3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9e7b3-107">EXAMPLES</span></span>

### <span data-ttu-id="9e7b3-108">예제 1: 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="9e7b3-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="9e7b3-109">이 명령은 SAS URL로 지정 된 blob에서 Azure Redis Cache로 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="9e7b3-110">변수</span><span class="sxs-lookup"><span data-stu-id="9e7b3-110">PARAMETERS</span></span>

### <span data-ttu-id="9e7b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7b3-111">-DefaultProfile</span></span>
<span data-ttu-id="9e7b3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e7b3-113">-파일</span><span class="sxs-lookup"><span data-stu-id="9e7b3-113">-Files</span></span>
<span data-ttu-id="9e7b3-114">이 cmdlet이 캐시로 가져오는 콘텐츠가 있는 blob의 SAS Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="9e7b3-115">다음 PowerShell 명령을 사용 하 여 SAS Url을 생성할 수 있습니다. $storageAccountContext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken-컨테이너 "containerName"-blob "blobName"-Permission "rwdl"-StartTime ([System: DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-Context $storageAccountContext-FullUri Import-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-Files ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="9e7b3-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="9e7b3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9e7b3-116">-Force</span></span>
<span data-ttu-id="9e7b3-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e7b3-118">-형식</span><span class="sxs-lookup"><span data-stu-id="9e7b3-118">-Format</span></span>
<span data-ttu-id="9e7b3-119">Blob 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="9e7b3-120">현재 rdb만 지원 되는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="9e7b3-121">-이름</span><span class="sxs-lookup"><span data-stu-id="9e7b3-121">-Name</span></span>
<span data-ttu-id="9e7b3-122">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="9e7b3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e7b3-123">-PassThru</span></span>
<span data-ttu-id="9e7b3-124">이 cmdlet이 작업 성공 여부를 나타내는 Boolean을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="9e7b3-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e7b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e7b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="9e7b3-127">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="9e7b3-128">-확인</span><span class="sxs-lookup"><span data-stu-id="9e7b3-128">-Confirm</span></span>
<span data-ttu-id="9e7b3-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e7b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e7b3-130">-WhatIf</span></span>
<span data-ttu-id="9e7b3-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e7b3-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e7b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7b3-133">CommonParameters</span></span>
<span data-ttu-id="9e7b3-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e7b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7b3-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e7b3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7b3-136">입력</span><span class="sxs-lookup"><span data-stu-id="9e7b3-136">INPUTS</span></span>

### <span data-ttu-id="9e7b3-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9e7b3-137">System.String</span></span>

### <span data-ttu-id="9e7b3-138">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="9e7b3-138">System.String[]</span></span>

## <span data-ttu-id="9e7b3-139">출력</span><span class="sxs-lookup"><span data-stu-id="9e7b3-139">OUTPUTS</span></span>

### <span data-ttu-id="9e7b3-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9e7b3-140">System.Boolean</span></span>

## <span data-ttu-id="9e7b3-141">상속자</span><span class="sxs-lookup"><span data-stu-id="9e7b3-141">NOTES</span></span>
* <span data-ttu-id="9e7b3-142">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="9e7b3-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9e7b3-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e7b3-143">RELATED LINKS</span></span>

[<span data-ttu-id="9e7b3-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e7b3-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="9e7b3-145">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e7b3-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="9e7b3-146">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e7b3-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="9e7b3-147">다시 설정-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e7b3-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="9e7b3-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e7b3-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


