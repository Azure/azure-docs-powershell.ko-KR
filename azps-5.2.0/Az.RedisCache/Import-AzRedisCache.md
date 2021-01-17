---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336489"
---
# <span data-ttu-id="d77fb-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d77fb-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="d77fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d77fb-102">SYNOPSIS</span></span>
<span data-ttu-id="d77fb-103">Blob에서 Azure Redis Cache로 데이터를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="d77fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="d77fb-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d77fb-105">설명</span><span class="sxs-lookup"><span data-stu-id="d77fb-105">DESCRIPTION</span></span>
<span data-ttu-id="d77fb-106">**Import-AzRedisCache** cmdlet은 Blob에서 Azure Redis Cache로 데이터를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="d77fb-107">예제</span><span class="sxs-lookup"><span data-stu-id="d77fb-107">EXAMPLES</span></span>

### <span data-ttu-id="d77fb-108">예제 1: 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="d77fb-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="d77fb-109">이 명령은 SAS URL에 의해 지정된 Blob에서 Azure Redis Cache로 데이터를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="d77fb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d77fb-110">PARAMETERS</span></span>

### <span data-ttu-id="d77fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77fb-111">-DefaultProfile</span></span>
<span data-ttu-id="d77fb-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d77fb-113">-Files</span><span class="sxs-lookup"><span data-stu-id="d77fb-113">-Files</span></span>
<span data-ttu-id="d77fb-114">이 cmdlet의 콘텐츠가 캐시로 가져오는 Blob의 SAS URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="d77fb-115">$storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now)을 사용하여 SAS URL을 생성할 수 있습니다. AddMinutes(-15) -ExpiryTime([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="d77fb-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="d77fb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d77fb-116">-Force</span></span>
<span data-ttu-id="d77fb-117">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d77fb-118">-Format</span><span class="sxs-lookup"><span data-stu-id="d77fb-118">-Format</span></span>
<span data-ttu-id="d77fb-119">Blob의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="d77fb-120">현재 rdb는 지원되는 유일한 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="d77fb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d77fb-121">-Name</span></span>
<span data-ttu-id="d77fb-122">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="d77fb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d77fb-123">-PassThru</span></span>
<span data-ttu-id="d77fb-124">이 cmdlet은 작업이 성공하는지 여부를 나타내는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="d77fb-125">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d77fb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d77fb-126">-ResourceGroupName</span></span>
<span data-ttu-id="d77fb-127">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="d77fb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d77fb-128">-Confirm</span></span>
<span data-ttu-id="d77fb-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d77fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d77fb-130">-WhatIf</span></span>
<span data-ttu-id="d77fb-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d77fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d77fb-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d77fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77fb-133">CommonParameters</span></span>
<span data-ttu-id="d77fb-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d77fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77fb-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d77fb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77fb-136">입력</span><span class="sxs-lookup"><span data-stu-id="d77fb-136">INPUTS</span></span>

### <span data-ttu-id="d77fb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d77fb-137">System.String</span></span>

### <span data-ttu-id="d77fb-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d77fb-138">System.String[]</span></span>

## <span data-ttu-id="d77fb-139">출력</span><span class="sxs-lookup"><span data-stu-id="d77fb-139">OUTPUTS</span></span>

### <span data-ttu-id="d77fb-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d77fb-140">System.Boolean</span></span>

## <span data-ttu-id="d77fb-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d77fb-141">NOTES</span></span>
* <span data-ttu-id="d77fb-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="d77fb-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d77fb-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d77fb-143">RELATED LINKS</span></span>

[<span data-ttu-id="d77fb-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d77fb-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="d77fb-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d77fb-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d77fb-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d77fb-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d77fb-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d77fb-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="d77fb-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d77fb-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


